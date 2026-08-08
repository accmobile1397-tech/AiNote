# AI Infrastructure Ecosystem Pattern

## Centralized Multi-Application AI Platform Infrastructure

**Pattern ID:** `INF-AI-PLATFORM-001`  
**Pattern Name:** Centralized AI Infrastructure Ecosystem  
**Category:** Infrastructure Architecture / AI Platform  
**Status:** Recommended Baseline  
**Scope:** Multi-Application / Multi-API AI Ecosystem

---

## 1. Intent

ایجاد یک زیرساخت مرکزی و قابل توسعه برای چندین Website و Application که بتوانند از خدمات AI از طریق یک **AI Gateway مرکزی** استفاده کنند، بدون وابستگی مستقیم به AI Providerها.

این Pattern برای اکوسیستم‌هایی مناسب است که چند Application مستقل دارند اما می‌خواهند:

- AI Infrastructure مشترک
- Data Infrastructure مشترک
- Monitoring مرکزی
- Provider Abstraction
- Usage Management
- Cost Management
- Future Local AI

داشته باشند.

---

## 2. Core Principle

اصل مرکزی:

> **Applications مستقل هستند؛ AI Infrastructure مرکزی است.**

Applicationها نباید مستقیماً به AI Providerها متصل شوند.

معماری:

```text
Applications
     │
     ▼
aifreeapi.ir
     │
     ▼
AI Gateway
     │
     ▼
AI Providers
```

---

## 3. Ecosystem Architecture

معماری فعلی:

```text
                              INTERNET
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
                    ▼                           ▼
             Public Websites              API Consumers
                    │                           │
                    └─────────────┬─────────────┘
                                  │
                                  ▼
                       ┌─────────────────────┐
                       │ 1. HOST SERVER      │
                       │      OpenShip       │
                       │                     │
                       │ Applications        │
                       │ Frontends           │
                       │ Application APIs    │
                       └──────────┬──────────┘
                                  │
                                  │ AI API
                                  ▼
                       ┌─────────────────────┐
                       │ 3. AI GATEWAY      │
                       │      SERVER        │
                       │                     │
                       │ Authentication     │
                       │ API Management     │
                       │ Rate Limit         │
                       │ Quota              │
                       │ Model Router       │
                       │ Provider Adapter   │
                       │ Load Balancing     │
                       │ Failover           │
                       │ Usage              │
                       │ Cost               │
                       │ Billing            │
                       └──────────┬──────────┘
                                  │
                    ┌─────────────┼─────────────┐
                    ▼             ▼             ▼
                  Qwen         DeepSeek      Other
                  Cloud         Cloud       Providers
                                                
                                                
         ┌────────────────────────────────────────────┐
         │ 2. DATA SERVER                             │
         │                                            │
         │ PostgreSQL                                 │
         │ Redis                                      │
         │ MinIO                                      │
         │ Vector Storage                             │
         │ Knowledge Service                          │
         └────────────────────────────────────────────┘


         ┌────────────────────────────────────────────┐
         │ 4. MONITORING SERVER                       │
         │                                            │
         │ Prometheus                                 │
         │ Grafana                                    │
         │ Loki                                       │
         │ Alertmanager                               │
         │ Exporters / Agents                         │
         └────────────────────────────────────────────┘
```

---

## 4. Infrastructure Layers

اکوسیستم به چهار لایه اصلی تقسیم می‌شود:

```text
Layer 1
Application Infrastructure
        ↓
Host / OpenShip

Layer 2
Data Infrastructure
        ↓
Data Server

Layer 3
AI Infrastructure
        ↓
AI Gateway Server

Layer 4
Observability Infrastructure
        ↓
Monitoring Server
```

این تفکیک باید حفظ شود.

---

## 5. Server 1 — Host / OpenShip

### Responsibility

Host Server محل اجرای Applicationها است.

شامل:

```text
Host Server
│
├── OpenShip
├── Websites
├── Frontends
├── Application APIs
├── Background Application Services
└── Other Application Containers
```

نمونه Applicationها:

```text
ComputerJobs
AIWebsiteBuilder
Other Websites
aifreeapi.ir Web Application
Future Applications
```

### اصل

Host Server مسئول **Application Runtime** است، نه AI Provider Runtime.

---

## 6. Server 2 — Data Server

Data Server مرکز داده مشترک اکوسیستم است.

```text
Data Server
│
├── PostgreSQL
├── Redis
├── MinIO
├── Vector Storage
└── Knowledge Service
```

### PostgreSQL

مرکز داده ساختاریافته:

```text
Users
APIs
API Keys Metadata
Plans
Usage
Costs
Billing
Knowledge Metadata
Application Data
```

### Redis

برای:

- Cache
- Rate Limiting
- Temporary State
- Queues
- Session/Short-lived Data

### MinIO

برای Object Storage:

- Documents
- Files
- Knowledge Assets
- Future AI Assets

### Vector Storage

برای Future:

- Embeddings
- Vector Search
- RAG

---

## 7. Knowledge Service

Knowledge از نظر Software Architecture یک Service مستقل است.

اما در MVP/مرحله فعلی Server مستقل ندارد.

```text
Application / AI Service
          │
          ▼
    Knowledge API
          │
          ▼
    Knowledge Service
          │
     ┌────┼─────┐
     ▼    ▼     ▼
 PostgreSQL Vector MinIO
```

در صورت رشد Workload:

```text
Current:

Data Server
 └── Knowledge Service


Future:

Knowledge Server
 └── Knowledge Service
```

API Contract نباید تغییر کند.

بنابراین:

> **Logical Separation First, Physical Separation Later.**

---

## 8. Server 3 — AI Gateway Server

AI Gateway قلب AI Infrastructure است.

```text
AI Gateway Server
│
├── API Authentication
├── API Key Validation
├── User/API Resolution
├── Authorization
├── Rate Limiting
├── Quota Enforcement
├── Model Router
├── Provider Abstraction
├── Load Balancing
├── Failover
├── Usage Metering
├── Cost Calculation
├── Billing Integration
└── Health / Observability Hooks
```

---

## 9. Public API Boundary

Applicationها نباید Gateway Server را مستقیماً ببینند.

Public contract:

```text
https://aifreeapi.ir/v1
```

Architecture:

```text
Application
    │
    ▼
aifreeapi.ir
    │
    ▼
Gateway Infrastructure
```

و نه:

```text
Application
    │
    ▼
Gateway Server IP
```

---

## 10. AI Provider Layer

Gateway می‌تواند به Providerهای مختلف متصل شود:

```text
AI Gateway
      │
      ├── Qwen
      ├── DeepSeek
      ├── GLM
      ├── Kimi
      ├── OpenAI
      ├── Other Cloud Providers
      │
      └── Future Local AI
```

Providerها قابل تعویض هستند.

Applicationها نباید از Provider آگاه باشند.

---

## 11. Current Provider Strategy

در MVP لازم نیست تعداد زیادی Provider متصل شوند.

الگوی پیشنهادی:

```text
Primary Provider
       ↓
Fallback Provider
       ↓
Additional Providers
```

مثلاً:

```text
Qwen
  ↓
DeepSeek
  ↓
Provider C
```

بعداً می‌توان Routing را توسعه داد:

- Weighted
- Latency Based
- Cost Based
- Capability Based
- Health Based

---

## 12. Server 4 — Monitoring Server

Monitoring یک زیرساخت مستقل است.

```text
Monitoring Server
│
├── Prometheus
├── Grafana
├── Loki
├── Alertmanager
└── Exporters / Agents
```

این Server باید وضعیت کل Ecosystem را مشاهده کند:

- Host Server
- Data Server
- AI Gateway Server
- Applications
- Providers
- PostgreSQL
- Redis
- MinIO
- Knowledge Service
- Network

---

## 13. Observability Flow

```text
Applications
      │
      ├──────────────┐
      │              │
      ▼              ▼
AI Gateway       Application Logs
      │              │
      └──────┬───────┘
             ▼
       Monitoring
             │
     ┌───────┼────────┐
     ▼       ▼        ▼
 Prometheus Grafana  Loki
```

---

## 14. Security Zones

Infrastructure باید به چند Security Zone تقسیم شود:

```text
Internet
   │
   ▼
Public Zone
   │
   ▼
Application / API Zone
   │
   ├── Host
   └── AI Gateway
          │
          ▼
     Private Data Zone
          │
          └── Data Server

Monitoring Zone
          │
          └── Monitoring Server
```

Databaseها نباید Public باشند.

Redis نباید Public باشد.

Provider Credentials نباید Public باشند.

---

## 15. Network Principle

ارتباطات داخلی ترجیحاً Private Network باشد:

```text
Host
 │
 ├──→ Data Server
 │
 ├──→ AI Gateway
 │
 └──→ Monitoring

AI Gateway
 │
 ├──→ Data Server
 ├──→ Monitoring
 └──→ Internet → Providers
```

Public Internet فقط باید به سرویس‌های Public لازم دسترسی داشته باشد.

---

## 16. Resource Allocation

### Host Server

منابع متناسب با تعداد Applicationها.

### Data Server

منابع بر اساس:

- PostgreSQL
- Redis
- MinIO
- Vector workloads
- Knowledge workloads

### AI Gateway

برای MVP:

```text
8 vCPU
16 GB RAM
100 GB NVMe
1 Gbps
Ubuntu 24.04
Docker
No GPU
```

### Monitoring

منابع متوسط و متناسب با حجم Metrics/Logs.

---

## 17. GPU Infrastructure

GPU Server فعلاً بخشی از Infrastructure اجرایی نیست.

در Roadmap آینده:

```text
AI Gateway
      │
      ├── Cloud Providers
      │
      └── GPU Server
              │
        ┌─────┴─────┐
        ▼           ▼
      Ollama       vLLM
        │           │
        ├── LLM     ├── LLM
        ├── Embedding
        └── Reranker
```

Gateway باید از ابتدا Provider-Agnostic باشد تا اضافه شدن GPU Server نیازی به تغییر Applicationها نداشته باشد.

---

## 18. Scaling Strategy

### Stage 1 — MVP

```text
Host × 1
Data × 1
Gateway × 1
Monitoring × 1
```

### Stage 2 — Gateway Scaling

```text
             Load Balancer
                   │
            ┌──────┴──────┐
            ▼             ▼
        Gateway #1     Gateway #2
```

### Stage 3 — Data Scaling

در صورت نیاز:

```text
PostgreSQL
Redis
MinIO
Vector
```

به‌صورت مستقل Scale شوند.

### Stage 4 — Knowledge Scaling

```text
Data Server
    │
    └── Knowledge Service
             ↓
      Dedicated Server
```

### Stage 5 — GPU Scaling

```text
AI Gateway
     │
     ├── Cloud AI
     │
     └── GPU Cluster
```

---

## 19. Stateless Gateway Principle

Gateway باید تا حد امکان Stateless باشد.

Stateهای مشترک:

```text
API Configuration
Usage
Quota
Rate Limit State
Sessions
Routing Configuration
```

باید در سرویس‌های مشترک قرار گیرند:

```text
PostgreSQL
Redis
```

این اصل امکان Horizontal Scaling را فراهم می‌کند.

---

## 20. Application Independence

تمام Applicationها باید یک الگوی یکسان داشته باشند:

```text
Application
    │
    ▼
aifreeapi.ir
    │
    ▼
AI Gateway
    │
    ▼
Provider
```

مثلاً:

```text
ComputerJobs ───────┐
                    │
AIWebsiteBuilder ───┤
                    │
Site C ─────────────┤
                    ▼
               aifreeapi.ir
                    │
                    ▼
               AI Gateway
                    │
                    ▼
                Providers
```

هیچ Application مسیر اختصاصی به Provider ندارد.

---

## 21. API Consumption Model

واحد مدیریت مصرف:

```text
User
 │
 ├── API: ComputerJobs
 │     ├── API Keys
 │     ├── Plan
 │     ├── Quota
 │     ├── Usage
 │     ├── Cost
 │     └── Billing
 │
 ├── API: Site A
 │
 └── API: Site B
```

Gateway Usage را در سطح API ثبت می‌کند.

---

## 22. Dogfooding

خود اکوسیستم باید از Gateway خودش استفاده کند.

```text
aifreeapi.ir
     │
     ▼
aifreeapi Gateway
     │
     ▼
Provider
```

همچنین:

```text
ComputerJobs
     │
     ▼
aifreeapi Gateway
```

این باعث می‌شود Gateway در محیط واقعی خودش تست شود.

---

## 23. Failure Isolation

اصل:

> شکست یک بخش نباید کل Ecosystem را از کار بیندازد.

مثال:

```text
Qwen DOWN
   ↓
Gateway
   ↓
DeepSeek
   ↓
SUCCESS
```

و:

```text
Provider Failure
      ≠
Gateway Failure
```

همچنین:

```text
Application Failure
      ≠
AI Infrastructure Failure
```

---

## 24. Backup Strategy

Data Server باید دارای Backup Strategy مستقل باشد.

حداقل:

```text
PostgreSQL
   ↓
Automated Backup

MinIO
   ↓
Object Backup / Replication

Configuration
   ↓
Version Controlled / Backup
```

Gateway Server نباید محل اصلی Backup Data باشد.

---

## 25. Deployment Pattern

تمام Infrastructure ترجیحاً Containerized باشد:

```text
Docker
   │
   ├── Host Applications
   ├── AI Gateway
   ├── Data Services
   └── Monitoring Services
```

Deployment باید قابل تکرار باشد.

Infrastructure Configuration نباید فقط در ذهن Administrator باشد.

---

## 26. Infrastructure Source of Truth

برای هر Server باید مشخص باشد:

```text
Purpose
Services
Network
Ports
Dependencies
Secrets
Backup
Monitoring
Scaling
Recovery
```

Infrastructure Documentation باید در Repository نگهداری شود.

---

## 27. Future Expansion

Architecture باید امکان تبدیل شدن به:

```text
AI Infrastructure Platform
```

را داشته باشد:

```text
                    AI Platform
                         │
       ┌─────────────────┼─────────────────┐
       ▼                 ▼                 ▼
   AI Gateway        Knowledge          Agent
       │              Services          Runtime
       │
       ├── LLM
       ├── Embedding
       ├── Image
       ├── Audio
       └── Video
```

اما هر سرویس باید استقلال منطقی خود را حفظ کند.

---

## 28. Core Architectural Rules

### Rule 1

> Applications مستقیم به AI Provider متصل نمی‌شوند.

### Rule 2

> Public API فقط از طریق `aifreeapi.ir` ارائه می‌شود.

### Rule 3

> AI Gateway از Application Hosting جداست.

### Rule 4

> Data Infrastructure از AI Gateway جداست.

### Rule 5

> Monitoring Infrastructure مستقل است.

### Rule 6

> Knowledge فعلاً Logical Service مستقل ولی روی Data Server است.

### Rule 7

> Gateway تا حد امکان Stateless طراحی می‌شود.

### Rule 8

> GPU Compute از Gateway جداست.

### Rule 9

> Provider قابل تعویض است.

### Rule 10

> Applicationها از تغییر Provider نباید آسیب ببینند.

### Rule 11

> APIهای داخلی و خارجی از یک Architecture استفاده می‌کنند.

### Rule 12

> aifreeapi.ir از Gateway خودش Dogfood می‌کند.

---

## 29. Final Ecosystem Pattern

```text
                              INTERNET
                                  │
                                  ▼
                    ┌────────────────────────┐
                    │      Public Layer      │
                    │                        │
                    │ aifreeapi.ir           │
                    │ Websites               │
                    └───────────┬────────────┘
                                │
                                ▼
                    ┌────────────────────────┐
                    │  HOST / OPENSHIP       │
                    │                        │
                    │ Applications           │
                    │ Frontends              │
                    │ Application APIs       │
                    └───────────┬────────────┘
                                │
                                ▼
                    ┌────────────────────────┐
                    │    AI GATEWAY SERVER   │
                    │                        │
                    │ Auth                   │
                    │ API Management         │
                    │ Routing                │
                    │ Rate Limit             │
                    │ Quota                  │
                    │ Usage                  │
                    │ Cost                   │
                    │ Billing                │
                    │ Health                 │
                    └───────────┬────────────┘
                                │
                       Provider Abstraction
                                │
                  ┌─────────────┼─────────────┐
                  ▼             ▼             ▼
                Qwen         DeepSeek      Providers


       ┌──────────────────────────────────────────┐
       │             DATA SERVER                   │
       │                                           │
       │ PostgreSQL                                │
       │ Redis                                     │
       │ MinIO                                     │
       │ Vector Storage                            │
       │ Knowledge Service                         │
       └──────────────────────────────────────────┘


       ┌──────────────────────────────────────────┐
       │          MONITORING SERVER               │
       │                                           │
       │ Prometheus                               │
       │ Grafana                                  │
       │ Loki                                     │
       │ Alertmanager                             │
       └──────────────────────────────────────────┘


                         FUTURE

       ┌──────────────────────────────────────────┐
       │              GPU SERVER                  │
       │                                           │
       │ Ollama / vLLM                            │
       │ Local LLM                                │
       │ Embeddings                               │
       │ Reranker                                 │
       └──────────────────────────────────────────┘
```

---

## 30. Pattern Statement

> **Centralized AI Infrastructure Ecosystem Pattern** یک معماری چندسروری برای اکوسیستم‌های دارای چند Application است که Application Hosting، Data Infrastructure، AI Gateway و Monitoring را از یکدیگر تفکیک می‌کند؛ در حالی که AI Gateway به‌عنوان تنها نقطه دسترسی Applicationها به AI Providers عمل می‌کند و امکان Provider Abstraction، Routing، Usage Management، Failover، Cost Management و توسعه آینده به Local AI، Knowledge و سایر AI Services را فراهم می‌سازد.

### Pattern Principle

> **Centralize the AI infrastructure, isolate responsibilities, keep applications provider-independent, and scale each infrastructure layer independently.**
