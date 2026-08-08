# My Project Preferences

## Version 2.1 — Reconstructed

> **Status:** Reconstructed  
> **Purpose:** Default project preferences for AI-assisted software projects  
> **Note:** This document reconstructs the previously used Version 2.1 based on available project knowledge, established decisions, and retained preferences. It should be treated as a working baseline until explicitly approved as the canonical version.

---

# 1. Purpose

این فایل شامل استانداردها، اصول، ترجیحات و تصمیمات پیش‌فرض برای شروع پروژه‌های جدید است.

هدف:

ایجاد یک روش ثابت برای:

- تحلیل
- طراحی
- معماری
- توسعه
- همکاری با AI

این موارد Default هستند و در صورت وجود دلیل فنی قابل تغییر هستند.

هر تغییر باید همراه با:

- دلیل
- مزایا
- معایب
- Trade-off

بررسی شود.

---

# 2. Product Owner Working Style

AI باید بداند Product Owner چگونه کار می‌کند.

Preferred approach:

- Guided Intelligence
- Step-by-Step Progress
- Clear Explanation
- Learning Through Building
- Decision Support

AI باید:

- گزینه ارائه دهد.
- مزایا و معایب را توضیح دهد.
- Trade-off را مشخص کند.
- پیشنهاد معماری بدهد.
- ریسک‌ها را مشخص کند.

AI فقط Code Generator نیست.

AI باید به عنوان:

- تحلیل‌گر
- مشاور
- معمار
- مستندساز
- اجراکننده

عمل کند.

---

# 3. General Philosophy

## Product Principles

- Vision First
- Business Model First
- User Value First
- User Centric First
- Scalability First
- AI First
- AI Native First
- Knowledge Base First

## Development Principles

- Documentation First
- Specification First
- Architecture First
- SDLC First
- Governance First
- API First
- Modular Architecture First
- Domain Driven Design Ready
- Event Driven Ready
- Open Standards First
- Vendor Lock-in Avoidance
- Source of Truth First

## Experience Principles

- UI First
- UX First
- Mobile First
- Responsive First
- Accessibility First
- Performance First
- SEO First
- Localization Ready
- RTL Ready

---

# 4. Knowledge Before Execution Principle

هیچ پروژه‌ای نباید با ایده خام وارد مرحله توسعه شود.

مدل:

```text
Knowledge
    ↓
Context
    ↓
Specification
    ↓
Execution
    ↓
Software
```

قبل از Code باید تا حد لازم موارد زیر وجود داشته باشد:

- Vision
- Requirements
- Architecture
- Decisions
- Specifications

هدف، جلوگیری از تبدیل مستقیم ایده به کد و کاهش rework است.

---

# 5. SDLC Governance

Default workflow:

```text
Vision
   ↓
PRD
   ↓
SRS
   ↓
Architecture Design
   ↓
Database Design
   ↓
API Design
   ↓
UI/UX Design
   ↓
Knowledge Base Setup
   ↓
Feature Specification
   ↓
Task Definition
   ↓
Implementation
   ↓
Testing
   ↓
Deployment
   ↓
Monitoring & Improvement
```

Rules:

- No coding before specification
- No feature without documentation
- No architecture decision without record
- Approved documents are Source of Truth
- Freeze Phase before implementation
- One Document at a Time
- MVP First
- Avoid Over Engineering

---

# 6. Specification Rules

Every feature requires a clear specification before implementation.

A feature specification should define, as applicable:

- Purpose
- User / Actor
- Business Goal
- User Value
- Functional Requirements
- Business Rules
- Inputs
- Outputs
- States
- Error Cases
- Permissions
- Dependencies
- API Requirements
- Data Requirements
- UI/UX Requirements
- AI Requirements
- Acceptance Criteria
- Non-Functional Requirements

Implementation should not begin while important ambiguities remain unresolved.

### Specification Principle

```text
Idea
 ↓
Requirement
 ↓
Specification
 ↓
Acceptance Criteria
 ↓
Task
 ↓
Implementation
```

---

# 7. Product Definition Rules

هر پروژه باید قبل از توسعه از نظر Product Definition روشن باشد.

حداقل موارد:

- Problem
- Target User
- User Need
- Proposed Solution
- Value Proposition
- Core User Journey
- Business Model
- Monetization
- MVP Scope
- Out of Scope
- Success Criteria

اصل:

> Build the smallest product that validates the most important assumption.

MVP نباید بهانه‌ای برای حذف معماری درست باشد، اما نباید شامل قابلیت‌های غیرضروری نیز باشد.

---

# 8. AI-Native Product Principles

AI در پروژه‌های جدید باید از ابتدا به‌عنوان یک قابلیت معماری در نظر گرفته شود، نه صرفاً یک API خارجی که بعداً اضافه می‌شود.

اصول:

- AI First
- AI Native
- AI Capability Abstraction
- AI Gateway First
- Multi-Model Ready
- Multi-Provider Ready
- Fallback Ready
- Local LLM Ready
- RAG Ready
- Embedding Ready
- AI Usage Tracking Ready

AI integration نباید مستقیماً در سراسر Application پخش شود.

ترجیح:

```text
Application
     ↓
AI Capability / AI Service
     ↓
AI Gateway / Provider Abstraction
     ↓
LLM / Embedding Provider
```

---

# 9. Agent Collaboration

در پروژه‌های AI-assisted، Agent نباید بدون Context کافی اقدام کند.

مدل همکاری:

```text
Human
  ↓
Product / Decision
  ↓
Specification
  ↓
AI Agent
  ↓
Implementation
  ↓
Verification
  ↓
Human Approval
```

AI Agent باید:

- Context را بخواند.
- Source of Truth را شناسایی کند.
- قبل از تغییر، Scope را مشخص کند.
- تغییرات را محدود به Task کند.
- Assumptionهای مهم را اعلام کند.
- نتیجه را گزارش کند.
- از تغییرات خارج از Scope خودداری کند.

---

# 10. Project Knowledge

Knowledge پروژه باید از Code جدا اما در ارتباط مستقیم با آن نگهداری شود.

Knowledge شامل:

- Vision
- Product Definition
- Requirements
- Architecture
- Decisions
- Specifications
- Business Rules
- Domain Knowledge
- API Contracts
- UX Rules
- AI Rules
- Operational Knowledge

اصل:

> Code is an implementation of knowledge, not the primary source of product intent.

---

# 11. Architecture Preferences

Default architecture preference:

- Modular Architecture
- Modular Monolith First
- Clear Module Boundaries
- Separation of Concerns
- Domain-oriented organization
- API-first
- Infrastructure abstraction
- External service abstraction

Microservices نباید Default باشند.

ابتدا:

```text
Modular Monolith
```

و فقط در صورت وجود نیاز واقعی:

```text
Modular Monolith
       ↓
Service Extraction
```

دلایل احتمالی برای استخراج Service:

- Independent Scaling
- Independent Deployment
- Strong Isolation
- Team Boundary
- Reliability Boundary
- Infrastructure Requirement

---

# 12. Technology Stack Preferences

Default preference برای Web Applicationهای جدید:

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui

### Backend

- Node.js
- TypeScript
- API-first architecture

### ORM

- Prisma

### Database

Relational Database به‌عنوان Default.

Database انتخابی باید بر اساس:

- Requirements
- Scale
- Ecosystem
- Operational Simplicity
- Cost

تعیین شود.

### Infrastructure

ترجیح:

- Docker
- Container-based Deployment
- Linux
- VPS / Cloud
- CI/CD

---

# 13. Database Preferences

Database باید بر اساس Domain و نیاز واقعی طراحی شود.

اصول:

- Relational First
- Explicit Schema
- Referential Integrity
- Proper Indexing
- Migration-based Changes
- Transaction Awareness
- Auditability Where Needed

Database نباید صرفاً بر اساس محبوبیت Technology انتخاب شود.

Schema باید قبل از Implementation قابلیت‌های اصلی مشخص شود.

---

# 14. Backend Preferences

Backend باید:

- Modular
- Typed
- API-first
- Testable
- Observable
- Secure

باشد.

Business Logic نباید مستقیماً در:

- UI Components
- Controllers
- Database Queries

پراکنده شود.

ترجیح:

```text
API
 ↓
Application / Use Case
 ↓
Domain Logic
 ↓
Infrastructure
```

تا حدی که Complexity پروژه توجیه کند.

---

# 15. Frontend Preferences

Frontend باید:

- Mobile First
- Responsive
- Accessible
- Performance-oriented
- Component-based
- Type-safe
- SEO-aware

باشد.

ترجیح:

- Reusable Components
- Design System
- Consistent UX
- Clear State Management
- Server-side capabilities where appropriate

UI نباید صرفاً برای Desktop طراحی و سپس Mobile شود.

---

# 16. API Preferences

API باید:

- Explicit
- Documented
- Versionable where required
- Secure
- Consistent
- Error-aware

باشد.

هر API باید مشخص کند:

- Request
- Response
- Validation
- Authentication
- Authorization
- Errors
- Rate Limits where applicable

ترجیح:

```text
UI
 ↓
API Contract
 ↓
Backend
```

و نه وابستگی مستقیم UI به implementation داخلی Backend.

---

# 17. AI Architecture Preferences

AI architecture باید قابلیت تغییر Provider و Model را داشته باشد.

ترجیح:

```text
Application
     ↓
AI Capability
     ↓
AI Gateway
     ↓
Provider Adapter
     ↓
Model
```

قابلیت‌های AI باید از Provider جدا باشند.

مثلاً:

```text
generateText()
generateStructuredOutput()
generateEmbedding()
moderateContent()
```

به جای اینکه Application مستقیماً با SDK یک Provider خاص کار کند.

### Required Capabilities

- Provider Abstraction
- Model Abstraction
- Fallback
- Timeout
- Retry
- Usage Tracking
- Token Tracking
- Cost Tracking where applicable
- Observability
- Error Handling

---

# 18. RAG / Knowledge Architecture

RAG و Knowledge System باید با AI Gateway اشتباه گرفته نشوند.

تفکیک ترجیحی:

```text
Application
    ↓
Knowledge / RAG Layer
    ↓
Embedding
    ↓
Vector Store
    ↓
AI Gateway
    ↓
LLM
```

Embedding و LLM دو Capability متفاوت هستند.

اصول:

- Embedding Lifecycle
- Embedding Versioning
- Re-indexing Strategy
- Retrieval Strategy
- Chunking Strategy
- Metadata
- Knowledge Source Tracking

RAG فقط زمانی اضافه شود که واقعاً نیاز محصول باشد.

---

# 19. Persian / Localization Preferences

برای پروژه‌های فارسی:

- Persian First
- RTL First
- Mobile First
- Jalali Calendar where appropriate
- Persian-friendly typography
- Vazirmatn preferred
- Proper Persian numerals where UX requires
- Localization-ready architecture

Localization نباید با Hard-code کردن متن‌های فارسی در Logic پیاده‌سازی شود.

ترجیح:

```text
Application Logic
      ↓
Localization Layer
      ↓
UI Language
```

---

# 20. Infrastructure Preferences

Default infrastructure:

- Linux
- Docker
- Docker Compose where appropriate
- VPS / Cloud
- Reverse Proxy
- HTTPS
- Environment-based Configuration
- Automated Backups
- Monitoring
- Logging

Secrets نباید داخل Repository قرار بگیرند.

Configuration باید از Code جدا باشد.

---

# 21. Development Tools Preferences

Preferred development environment:

- Cursor
- GitHub
- Git
- AI-assisted development
- CLI tools where appropriate

AI coding tools باید در چارچوب SDLC و Specification استفاده شوند.

AI نباید جایگزین:

- Product Decision
- Architecture Decision
- Human Approval

شود.

---

# 22. Git / Repository Preferences

هر پروژه باید Repository مشخص داشته باشد.

اصول:

- Meaningful Commits
- Clear Commit Messages
- Small Logical Changes
- Documentation in Repository
- Source of Truth in Git
- Avoid Unrelated Changes

ترجیح می‌شود Commitها نشان‌دهنده یک تغییر منطقی باشند.

مثلاً:

```text
docs: add product vision
docs: define authentication requirements
feat: implement user registration
fix: handle invalid OTP
```

---

# 23. Testing & Quality Preferences

Testing باید متناسب با Risk و Complexity انجام شود.

سطوح:

- Unit Tests
- Integration Tests
- API Tests
- E2E Tests
- AI Evaluation where applicable

کیفیت فقط به Passing Tests محدود نیست.

Quality شامل:

- Correctness
- Security
- Performance
- Maintainability
- UX
- Accessibility
- Reliability

است.

---

# 24. Security Preferences

Security باید از ابتدا در Architecture لحاظ شود.

اصول:

- Least Privilege
- Secure Authentication
- Authorization
- Input Validation
- Output Validation
- Secret Management
- Rate Limiting
- Abuse Prevention
- Secure Defaults
- Auditability where needed

هیچ Secret یا Credential نباید در:

- Source Code
- Git History
- Documentation عمومی

قرار گیرد.

---

# 25. Documentation Preferences

Documentation باید بخشی از Product باشد، نه فعالیت جانبی.

مستندات مهم:

- README
- Vision
- Product Definition
- PRD
- SRS
- Architecture
- ADR
- API Specification
- Feature Specification
- Task
- Review
- Deployment Documentation

Documentation باید:

- قابل‌خواندن
- قابل‌جست‌وجو
- Version-controlled
- به‌روز

باشد.

---

# 26. Deployment & Operations Preferences

Deployment باید قابل تکرار باشد.

ترجیح:

```text
Code
 ↓
Build
 ↓
Test
 ↓
Container
 ↓
Deployment
 ↓
Health Check
 ↓
Monitoring
```

Production باید دارای حداقل:

- Logging
- Error Monitoring
- Health Checks
- Backup
- Recovery Strategy
- Resource Monitoring

باشد.

---

# 27. General Decision Rules

هر تصمیم مهم باید با توجه به موارد زیر بررسی شود:

1. Product Value
2. User Value
3. Simplicity
4. Maintainability
5. Scalability
6. Security
7. Performance
8. Cost
9. Vendor Lock-in
10. Future Flexibility

### Decision Priority

در صورت تعارض:

```text
User / Product Value
        ↓
Correctness
        ↓
Security
        ↓
Simplicity
        ↓
Maintainability
        ↓
Scalability
        ↓
Optimization
```

این ترتیب Absolute نیست و بسته به Context قابل تغییر است.

---

# 28. Final Default Rule

این فایل **Default Preference** است، نه قانون مطلق.

اصل نهایی:

> Use the simplest architecture and technology that correctly solves the current problem while preserving reasonable paths for future evolution.

اگر تصمیم جدیدی با این Preferences مغایرت داشت، نباید صرفاً به دلیل این سند رد شود.

باید بررسی شود:

- چرا تغییر لازم است؟
- چه مشکلی را حل می‌کند؟
- چه مزیتی دارد؟
- چه معایبی دارد؟
- چه Trade-offهایی ایجاد می‌کند؟
- آیا این تصمیم فقط برای همین پروژه است یا باید به Preference عمومی تبدیل شود؟

پس:

```text
Default
   ↓
Context
   ↓
Analysis
   ↓
Trade-off
   ↓
Decision
   ↓
Record
```

و در نهایت:

> **Project-specific decisions override generic preferences when justified and documented.**

---

## Document Status

**Version:** 2.1  
**Reconstruction:** Yes  
**Canonical:** No — pending review  
**Intended Repository:** `AiNote`  
**Intended Path:** `knowledge/project-preferences/my-project-preferences-v2.1.md`
