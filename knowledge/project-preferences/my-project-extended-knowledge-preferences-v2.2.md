# My Project Extended Knowledge Preferences

## Version 2.2

# AI Native Software Factory Pattern Library

## 1. Purpose

این فایل شامل دانش‌های توسعه‌یافته، الگوهای اجرایی، تجربیات انباشته‌شده و روش‌های حل مسئله قابل استفاده مجدد برای پروژه‌های آینده است.

این سند مکمل:

**My Project Preferences**

است.

### تفاوت

**My Project Preferences** شامل:

- Principles
- Rules
- Defaults
- Standards

است.

**My Project Extended Knowledge Preferences** شامل:

- Patterns
- Practices
- Workflows
- Reusable Solutions
- Lessons Learned
- AI-native Project Methods

است.

هدف:

تبدیل تجربه‌های پروژه‌ها به دانش قابل استفاده مجدد برای ساخت سریع‌تر، باکیفیت‌تر و هوشمندانه‌تر پروژه‌های AI-native.

---

## 2. Pattern Evolution Model

هر دانش جدید باید از چرخه زیر عبور کند:

```text
Experience
↓
Documentation
↓
Review
↓
Approved Pattern
↓
Reusable Knowledge
```

هدف:

تبدیل تجربه پروژه‌ها به سرمایه دانشی قابل استفاده مجدد.

---

## 3. Brain Before Body Pattern

### Purpose

جلوگیری از شروع توسعه قبل از ایجاد درک کافی از پروژه.

### Principle

نرم‌افزار قبل از ساخته شدن باید دارای «مغز» باشد.

### Model

```text
Idea
↓
Project Knowledge Base
↓
AI Agents
↓
Specification
↓
Implementation
↓
Software Product
```

### Rules

- AI Developer نباید با ایده خام شروع کند.
- Context باید قبل از Code ایجاد شود.
- Knowledge باید قبل از Execution شکل بگیرد.
- Specification باید قبل از Implementation وجود داشته باشد.

---

## 4. Project Knowledge Base Pattern

### Purpose

ایجاد یک لایه دانش مرکزی برای پروژه.

Project Knowledge Base شامل:

- Business Knowledge
- Product Knowledge
- Technical Knowledge
- Operational Knowledge
- Decision History

### مصرف‌کنندگان

- Human Team
- AI Assistant
- AI Agents
- RAG Systems
- Local LLM

Project Knowledge Base باید قابل استفاده برای تولید Context مورد نیاز Agentها باشد.

---

## 5. Project Operating Memory Pattern

### Purpose

ایجاد حافظه دائمی برای پروژه‌های AI-native.

### Principle

**Project Should Remember**

یک پروژه نباید با تغییر:

- Chat
- Agent
- Tool
- Developer

Context خود را از دست بدهد.

### Structure

```text
Project Operating Memory
├── Knowledge Layer
├── State Layer
├── Decision Layer
├── Execution Layer
└── Learning Layer
```

### Benefits

- حفظ Context پروژه
- همکاری چند Agent
- بازیابی تصمیمات گذشته
- یادگیری مستمر
- افزایش کیفیت تصمیم‌ها

---

## 6. Three Layer Knowledge Architecture Pattern

### Purpose

مدیریت دانش پروژه در سه سطح مستقل.

### Architecture

```text
General Project Knowledge
        ↓
Project Specific Knowledge
        ↓
Project Operating Memory
```

### General Project Knowledge

دانش عمومی و قابل استفاده مجدد.

Examples:

- SDLC Protocol
- Agent Rules
- Architecture Principles
- UI Principles
- Security Patterns
- Development Standards
- Reusable Patterns

### Project Specific Knowledge

دانش اختصاصی هر محصول.

Examples:

- Vision
- Product Rules
- User Journeys
- Business Rules
- Design System
- Architecture Decisions

### Project Operating Memory

حافظه عملیاتی پروژه.

Examples:

- Current Phase
- Roadmap Status
- Tasks
- Decisions
- Reports
- Lessons Learned

---

## 7. Foundation Knowledge Before Development Pattern

### Purpose

ایجاد حداقل دانش لازم قبل از شروع توسعه.

قبل از واگذاری پروژه به Developer Agent ممکن است مجموعه‌ای از Foundation / Anchor Documents ایجاد شود.

در پروژه‌های پیچیده، این مجموعه می‌تواند حدود 25 تا 40 سند یا بیشتر باشد؛ این عدد یک Guideline است و الزام ثابت نیست.

شامل مواردی مانند:

- Vision
- Product Definition
- Business Model
- Personas
- Requirements
- Architecture Baseline
- Technology Decisions
- AI Strategy
- Security Principles
- UX Principles
- Project Governance

هدف:

ایجاد تصمیم و Context، نه تولید تمام جزئیات اجرایی پروژه.

---

## 8. Documentation Evolution Pattern

### Principle

مستندات پروژه در دو مرحله اصلی رشد می‌کنند.

### Before Development

تمرکز:

- تصمیم‌گیری
- اصول
- معماری
- تجربه کاربری
- Product Definition
- Foundation Knowledge

در پروژه‌های مختلف تعداد اسناد می‌تواند متفاوت باشد.

### During Development

تمرکز:

- Feature Specification
- Tasks
- Reports
- Testing
- Evidence
- Reviews
- Operational Documentation

ممکن است صدها سند تولید شود.

هدف:

> ما تولیدکننده دستی همه مستندات نیستیم؛ ما سیستم تولید و نگهداری مستندات می‌سازیم.

---

## 9. Specification → Execution Pattern

### Workflow

```text
Vision
↓
PRD
↓
SRS
↓
Architecture
↓
Feature Specification
↓
Task
↓
Code
↓
Test
↓
Review
```

### Rules

- هر Task باید Specification داشته باشد.
- هر Code باید Task داشته باشد.
- هر Feature باید Documentation داشته باشد.

---

## 10. Source of Truth Pattern

### Principle

هر پروژه باید یک مرجع حقیقت مشخص داشته باشد.

### Sources

- Anchor Documents
- Approved Documentation
- Specifications
- Decision Records
- Project State
- Task Records
- Source Code

تصمیم‌ها نباید فقط در:

- Chat
- Memory
- Messages

باقی بمانند.

---

## 11. Project State Layer Pattern

### Purpose

Agentها باید همیشه بدانند پروژه در چه وضعیتی است.

State شامل:

- Current Phase
- Current Milestone
- Current Task
- Roadmap Status
- Completed Work
- Current Work
- Pending Work
- Blockers
- Next Actions

### Rule

State باید بعد از هر Task یا هر تغییر معنادار پروژه به‌روزرسانی شود.

### Model

```text
Read State
↓
Execute Task
↓
Validate Result
↓
Create Report
↓
Update State
↓
Continue
```

---

## 12. Multi Roadmap Pattern

Roadmapها در سطوح مختلف ایجاد می‌شوند.

### Master Project Roadmap

در شروع پروژه ایجاد می‌شود.

هدف:

نمای کلی مسیر پروژه.

### Phase Roadmap

توسط Agent مسئول آن Phase ایجاد می‌شود.

مدل:

```text
Phase Start
↓
Analyze Current State
↓
Create Phase Roadmap
↓
Create Tasks
↓
Execute
```

### Task Roadmap

سطح اجرای عملیاتی و روزانه است.

---

## 13. AI Assisted Decision Pattern

در تصمیم‌های مهم AI باید ارائه دهد:

- Context
- Options
- Benefits
- Risks
- Trade-offs
- Recommendation

تصمیم نهایی باید ثبت شود.

---

## 14. Human Non-Blocking Pattern

### Principle

انسان نباید به صورت غیرضروری گلوگاه Workflow باشد.

### Model

```text
Agent Work
↓
Self Validation
↓
Report
↓
State Update
↓
Continue
```

Human Review می‌تواند برای:

- Strategic Decisions
- Quality Improvement
- Risk Management
- Approval of Major Changes

استفاده شود.

هدف:

حفظ Human Governance بدون تبدیل کردن انسان به گلوگاه اجرای تمام Taskها.

---

## 15. AI Agent Pattern

هر Agent باید تعریف داشته باشد:

- Role
- Goal
- Context
- Tools
- Memory
- Permissions
- Evaluation Criteria

Agentها باید:

- محدود باشند.
- قابل ارزیابی باشند.
- قابل جایگزینی باشند.

---

## 16. Multi Agent Collaboration Pattern

ساختار پیشنهادی:

```text
Orchestrator
├── Product Agent
├── Architecture Agent
├── Documentation Agent
├── Engineering Agent
├── QA Agent
├── DevOps Agent
├── Security Agent
└── SEO Agent
```

Agentها باید از Project Knowledge Base و Project Operating Memory به عنوان Context استفاده کنند.

---

## 17. AI Gateway Pattern

### Purpose

جدا کردن Application از AI Provider.

### Architecture

```text
Application
↓
AI Gateway
↓
Provider Adapter
↓
AI Providers
```

پشتیبانی:

- Cloud Models
- OpenAI Compatible APIs
- Local LLM
- Ollama
- Future Providers

### مزایا

- کاهش هزینه
- تغییر Provider
- Fallback
- Multi Model Strategy
- Vendor Lock-in Avoidance

---

## 18. External AI Gateway Integration Pattern

### Purpose

در پروژه‌هایی که یک AI Gateway Platform مرکزی در اختیار دارند، Application نباید مستقیماً با AI Providerها ارتباط داشته باشد.

### Architecture

```text
Project Application
↓
External AI Gateway Platform
↓
Provider Adapter
↓
AI Providers
```

نمونه:

```text
ComputerJobs
↓
aifreeapi.ir
↓
AI Gateway Platform
↓
OpenAI / GLM / Ollama / Local LLM
```

### Principle

Application باید به AI Capability / API Contract وابسته باشد، نه به Provider خاص.

Application نباید بداند:

- Provider چگونه انتخاب می‌شود.
- Fallback چگونه انجام می‌شود.
- Provider API چگونه کار می‌کند.
- Embedding Model کدام است.
- Vector Infrastructure چگونه پیاده شده است.

این مسئولیت‌ها متعلق به AI Gateway Platform هستند.

### Benefits

- Provider Independence
- Centralized AI Infrastructure
- Centralized Cost Management
- Centralized Usage Tracking
- Fallback
- Model Routing
- Shared RAG Infrastructure
- Shared AI Services
- کاهش Vendor Lock-in

### Trade-off

وابستگی به Gateway Platform ایجاد می‌شود؛ بنابراین:

- API Contract باید مستند و پایدار باشد.
- Gateway باید قابل جایگزینی باشد.
- Application نباید به Implementation داخلی Gateway وابسته شود.

---

## 19. AI Capability Abstraction Pattern

### Purpose

جلوگیری از وابستگی Application به مدل یا Provider مشخص.

به جای:

```text
Application → GPT
```

یا:

```text
Application → GLM
```

از Capability استفاده شود:

```text
Application
↓
AI Capability
↓
AI Gateway
↓
Provider
```

Examples:

- Career Advisor
- Resume Analyzer
- Job Matching
- Text Generation
- Classification
- Summarization
- Structured Generation

Application باید نیاز خود را به صورت Capability تعریف کند.

Gateway مسئول انتخاب Model / Provider مناسب است.

---

## 20. LLM & Embedding Separation Pattern

### Principle

LLM و Embedding دو قابلیت مستقل هستند.

LLM:

```text
LLM
↓
Generate / Reason / Answer
```

در مقابل:

```text
Embedding
↓
Text → Vector
```

### Architecture

```text
AI Gateway
├── LLM Gateway
│   ├── OpenAI
│   ├── GLM
│   └── Ollama
│
└── Embedding Gateway
    ├── Local Embedding Models
    └── Cloud Embedding Models
```

### Rule

تغییر LLM Provider معمولاً نباید باعث Re-index شدن Knowledge Base شود.

مثال:

```text
GLM → OpenAI
```

نیازی به Re-index ندارد، اگر Embedding Model ثابت بماند.

---

## 21. RAG & Embedding Lifecycle Pattern

### Purpose

مدیریت استاندارد چرخه تولید و نگهداری Embeddingها.

### Pipeline

```text
Documents
↓
Chunking
↓
Embedding Model
↓
Vectors
↓
Vector Database
```

### Query

```text
User Query
↓
Same Embedding Space
↓
Vector Search
↓
Retrieved Context
↓
LLM
↓
Answer
```

### Automatic Embedding

Embedding باید به صورت Pipeline / Worker اتوماتیک انجام شود.

مثلاً:

```text
New Document
↓
Ingestion
↓
Chunking
↓
Embedding
↓
Vector Storage
```

انسان نباید برای هر سند به صورت دستی Embedding ایجاد کند.

---

## 22. Embedding Versioning & Re-indexing Pattern

### Principle

هر Vector باید مشخص کند با چه Embedding Model و Version تولید شده است.

### Metadata پیشنهادی

```text
document_id
chunk_id
embedding_model
embedding_version
created_at
```

### Re-index Trigger

اگر Embedding Model تغییر کند:

```text
Embedding Model A
↓
Embedding Model B
```

Vector Index باید مجدداً تولید شود.

### Re-index Workflow

```text
Select New Embedding Model
↓
Create New Index
↓
Read Documents
↓
Chunk / Re-chunk if required
↓
Generate New Embeddings
↓
Store New Vectors
↓
Validate Retrieval Quality
↓
Switch Active Index
↓
Retire Old Index
```

### Important Rule

Re-indexing به معنی تولید دوباره Documents نیست.

فقط Representation معنایی آنها دوباره تولید می‌شود.

### LLM Change vs Embedding Change

#### LLM Change

```text
GLM → OpenAI
```

معمولاً:

**No Re-index**

#### Embedding Change

```text
Embedding Model A → Model B
```

معمولاً:

**Re-index Required**

---

## 23. RAG Service Pattern

### Purpose

جدا کردن Knowledge Retrieval از Application.

### Architecture

```text
Application
↓
RAG Service
↓
Knowledge Base
↓
Embedding
↓
Vector Search
↓
Context
↓
LLM
```

RAG Service می‌تواند مسئول:

- Document Ingestion
- Chunking
- Embedding
- Vector Storage
- Retrieval
- Context Building
- Re-indexing
- Retrieval Evaluation

باشد.

Application فقط باید با RAG Contract کار کند.

---

## 24. Reusable Primitive Pattern

راه‌حل‌های تکرارشونده باید تبدیل به Primitive شوند.

Examples:

- Authentication
- Authorization
- Profile
- Payment
- Notification
- Search
- Dashboard
- Subscription
- AI Gateway
- RAG
- AI Assistant

هدف:

عدم طراحی مجدد قابلیت‌های تکرارشونده.

---

## 25. Modular Monolith Pattern

برای MVP:

```text
Modular Monolith
↓
Scale When Needed
↓
Service Extraction
```

مزایا:

- سرعت توسعه
- سادگی
- آمادگی رشد
- کاهش Operational Complexity

---

## 26. Domain Modeling Pattern

هر Domain باید مشخص کند:

- Entity
- Relationship
- Lifecycle
- Ownership
- Events

Examples:

- User
- Job
- Location
- Subscription
- Notification

---

## 27. Search Intelligence Evolution Pattern

مسیر تکامل:

```text
Keyword Search
↓
Advanced Search
↓
Semantic Search
↓
Vector Search
↓
RAG
```

هر مرحله فقط در صورت وجود نیاز واقعی اضافه شود.

---

## 28. Knowledge Evolution Pattern

Knowledge Base باید زنده باشد.

چرخه:

```text
Knowledge v1
↓
Development Feedback
↓
New Decision
↓
Knowledge v2
```

Knowledge باید از تجربه واقعی پروژه تغذیه شود.

---

## 29. Testing Strategy Pattern

استاندارد:

- Unit Testing
- Integration Testing
- E2E Testing
- AI Generated Testing
- Quality Validation
- AI Evaluation / Evals

برای قابلیت‌های AI باید علاوه بر تست نرم‌افزاری، کیفیت خروجی AI نیز قابل ارزیابی باشد.

---

## 30. Deployment Pattern

اولویت:

- Self Hosted
- Docker
- Linux
- VPS
- CI/CD
- Backup
- Monitoring
- Observability

---

## 31. Pattern Library Rule

هر Pattern جدید باید شامل:

- Name
- Purpose
- Context
- Problem
- Solution
- Benefits
- Trade-offs
- Examples

باشد.

Patternهای وابسته به Provider یا Technology خاص باید تا حد امکان به صورت Technology-Agnostic نوشته شوند.

---

## 32. Generalization Rule

دانش یک پروژه فقط زمانی وارد این Library شود که قابلیت استفاده مجدد داشته باشد.

مدل:

```text
Project Experience
↓
Extract General Principle
↓
Remove Project-Specific Details
↓
Review
↓
Approved Pattern
↓
Reusable Knowledge
```

هدف:

جلوگیری از تبدیل Pattern Library به مستندات یک پروژه خاص.

---

# Final Goal

ایجاد یک کتابخانه دانش نرم‌افزاری که باعث شود پروژه‌های آینده:

- سریع‌تر شروع شوند.
- Context کافی قبل از Development داشته باشند.
- تصمیم‌های بهتر بگیرند.
- اشتباهات تکراری کاهش یابد.
- AI Provider-independent باشند.
- RAG و AI Infrastructure قابل تعویض داشته باشند.
- آماده همکاری با AI Agents باشند.
- قابلیت تبدیل شدن به Factory Input را داشته باشند.

این Library باید به مرور به یک General AI-Native Software Engineering Knowledge Layer تبدیل شود که توسط:

- Human Developers
- AI Assistants
- AI Agents
- Documentation Agents
- Coding Agents
- Local LLMs
- AI Software Factory

قابل استفاده باشد.

---

**End of Document — Version 2.2**
