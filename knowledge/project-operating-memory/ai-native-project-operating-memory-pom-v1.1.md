# AI Native Project Operating Memory (POM)

## Version 1.1

**Project Memory Architecture Template**

> **AI WRITER INSTRUCTION**  
> If this document does not exist: Create it with the following content. If this document already exists: Update it to this version.  
> Target Path: `AI Native Project Operating Memory (POM).md`  
> Purpose: Define the standard operating memory architecture for AI-native software projects. Do not modify unrelated documents.

---

## 1. Purpose

AI Native Project Operating Memory (POM) یک معماری استاندارد برای مدیریت حافظه، دانش، وضعیت، تصمیمات، فعالیت‌ها و تجربیات یک پروژه نرم‌افزاری AI-native است.

هدف:

ایجاد یک لایه حافظه مرکزی که:

- Human Team
- AI Assistants
- AI Agents
- Development Tools
- RAG Systems
- Local LLMs

بتوانند از آن به عنوان Context قابل اعتماد استفاده کنند.

---

## 2. Core Principle

**Project Should Remember**

یک پروژه AI-native نباید با تغییر:

- Chat Session
- AI Model
- Agent
- Developer
- Tool

از صفر شروع شود.

تمام دانش، تصمیمات، وضعیت و تجربیات باید خارج از Conversation ذخیره و قابل بازیابی باشند.

مدل:

```text
Project Activity
      ↓
Project Operating Memory
      ↓
Future Decisions
      ↓
Continuous Improvement
```

---

## 3. POM Position in Project Architecture

POM جایگزین Documentation نیست.

POM سیستم مدیریت چرخه زندگی دانش پروژه است.

رابطه:

```text
Project Operating Memory
        ↓ Manages
Project Documentation
Decision Records
Tasks
Reports
Learning
```

مدل کامل:

```text
POM
├── Knowledge Layer
├── State Layer
├── Decision Layer
├── Execution Layer
└── Learning Layer

Documentation System
├── Vision
├── PRD
├── SRS
├── Architecture
├── UX
├── API
└── Specifications
```

---

## 4. POM Architecture

ساختار اصلی:

```text
AI Native Project Operating Memory
├── 01. Project Knowledge Base
├── 02. Project State Layer
├── 03. Decision History
├── 04. Execution History
└── 05. Learning History
```

---

## 5. Project Knowledge Base

### Purpose

حافظه دانشی پروژه.

شامل تمام اطلاعات پایه‌ای که برای درک پروژه لازم است.

ساختار:

```text
Project Knowledge Base
├── Vision
├── Product Definition
├── Product Rules
├── Business Knowledge
├── User Knowledge
├── Domain Knowledge
├── Architecture Principles
├── Technical Standards
└── AI Knowledge
```

### 5.1 Vision

شامل:

- Problem Statement
- Product Vision
- Goals
- Success Criteria
- Long Term Direction

### 5.2 Product Knowledge

شامل:

- Product Requirements
- Features
- User Roles
- User Journeys
- Business Rules

### 5.3 Business Knowledge

شامل:

- Business Model
- Monetization Rules
- Market Understanding
- Competitive Knowledge

### 5.4 Architecture Knowledge

شامل:

- Architecture Decisions
- Technology Choices
- System Principles
- Integration Rules

---

## 6. Project State Layer (PSL)

### Purpose

حافظه وضعیت فعلی پروژه.

Agentها باید بدانند:

- پروژه اکنون کجاست.
- چه چیزی تمام شده.
- چه چیزی در حال انجام است.
- قدم بعدی چیست.

ساختار:

```text
Project State Layer
├── Current Phase
├── Current Milestone
├── Current Task
├── Roadmap Status
├── Completed Work
├── Current Work
├── Pending Work
├── Blockers
└── Next Actions
```

---

## 7. Task State Management Rule

هر Agent باید قبل و بعد از هر Task وضعیت را مدیریت کند.

### Before Task

Agent باید بخواند:

- Current State
- Current Roadmap
- Relevant Knowledge

### After Task

Agent باید ثبت کند:

- Task Result
- Generated Artifacts
- Execution Report
- Updated State

چرخه:

```text
Read State
    ↓
Execute Task
    ↓
Validate
    ↓
Report
    ↓
Update State
    ↓
Continue
```

---

## 8. Decision History

### Purpose

ثبت تاریخچه تصمیمات مهم.

هیچ تصمیم مهمی نباید فقط در:

- Chat
- Memory
- Conversation

باقی بماند.

ساختار:

```text
Decision History
├── ADRs
├── Product Decisions
├── Architecture Decisions
├── Technology Decisions
├── UX Decisions
└── Trade-offs
```

### Decision Record Structure

هر تصمیم شامل:

- Context
- Problem
- Options
- Evaluation
- Decision
- Benefits
- Risks
- Trade-offs
- Date
- Owner

---

## 9. Execution History

### Purpose

ثبت فعالیت‌های اجرایی پروژه.

ساختار:

```text
Execution History
├── Tasks
├── Task Specifications
├── Task Reports
├── Reviews
├── Changes
├── Releases
└── Deployment History
```

---

## 10. Learning History

### Purpose

تبدیل تجربه پروژه به دانش آینده.

ساختار:

```text
Learning History
├── Lessons Learned
├── Patterns Discovered
├── Failed Approaches
├── Improvements
└── Future Recommendations
```

---

## 11. AI Agent Interaction Model

Agentها باید از POM به عنوان Memory Layer استفاده کنند.

مدل:

```text
AI Agent
   ↓
Read Project Operating Memory
   ↓
Analyze Context
   ↓
Generate Decision / Action
   ↓
Write Back Knowledge
   ↓
Update Memory
```

---

## 12. Agent Context Recovery Rule

هر Agent جدید باید بتواند بدون دسترسی به Conversationهای قبلی Context پروژه را بازیابی کند.

حداقل ورودی:

```text
PROJECT_CONTEXT
+
PROJECT_STATE
+
KNOWLEDGE_INDEX
+
CURRENT_TASK
```

---

## 13. Roadmap Management

Roadmapها چند سطح دارند.

### Master Project Roadmap

در شروع پروژه تعریف می‌شود.

هدف:

نمای کلی چرخه عمر پروژه.

### Phase Roadmap

توسط Agent مسئول همان Phase تولید می‌شود.

مدل:

```text
Phase Start
    ↓
Read Previous State
    ↓
Analyze Inputs
    ↓
Create Phase Roadmap
    ↓
Create Tasks
    ↓
Execute
```

### Task State

سطح اجرایی روزانه پروژه است.

---

## 14. Source of Truth

در پروژه AI-native:

اولویت منابع حقیقت:

```text
Anchor Documents
        ↓
Decision Records
        ↓
Approved Specifications
        ↓
Task Records
        ↓
Source Code
        ↓
Learning History
```

---

## 15. Relationship With Agentic SDLC

POM در تمام چرخه SDLC استفاده می‌شود.

```text
Vision Phase
    ↓
Knowledge Base
    ↓
Planning Phase
    ↓
State + Decisions
    ↓
Development Phase
    ↓
Tasks + Execution History
    ↓
Review Phase
    ↓
Learning History
    ↓
Updated Memory
```

---

## 16. Memory Update Rules

هر تغییر مهم باید باعث بررسی POM شود.

موارد نیازمند Update:

- New Feature
- Architecture Change
- Business Rule Change
- Technology Change
- New Decision
- New Lesson Learned
- New Pattern Discovery

---

## 17. Project Memory Evolution

POM یک سند ثابت نیست.

چرخه:

```text
POM v1
   ↓
Development Experience
   ↓
New Knowledge
   ↓
New Decisions
   ↓
POM v2
```

---

## 18. Minimum Required POM

هر پروژه جدید حداقل باید داشته باشد:

```text
01 Vision
02 Product Knowledge
03 Architecture Knowledge
04 Decision Records
05 Project State
06 Task History
07 Lessons Learned
```

---

## Final Goal

ایجاد پروژه‌هایی که:

- Context خود را حفظ می‌کنند.
- تصمیمات گذشته را فراموش نمی‌کنند.
- توسط AI Agents قابل مدیریت هستند.
- از تجربه‌های قبلی یاد می‌گیرند.
- به مرور هوشمندتر می‌شوند.

Project Operating Memory مغز عملیاتی پروژه است.

AI Agents موتور اجرای پروژه هستند.

بدون Memory، Agent فقط یک اجراکننده است؛  
با Memory، Agent تبدیل به عضو دائمی تیم پروژه می‌شود.

---

**End of Document — Version 1.1**
