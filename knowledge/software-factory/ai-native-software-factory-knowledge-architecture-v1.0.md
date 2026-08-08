# AI Native Software Factory Knowledge Architecture

## Version 1.0

---

# 1. Purpose

این سند معماری کلان دانش و فرآیند ساخت نرم‌افزار در محیط AI-native را تعریف می‌کند.

هدف:

ایجاد یک مدل استاندارد که در آن:

- Human
- AI Assistant
- AI Writer
- AI Documentation Developer
- AI Developer
- AI Agents
- Development Tools

بتوانند با یک ساختار مشخص همکاری کنند.

این سند توضیح می‌دهد چگونه:

ایده

به

دانش

سپس

مستندات

سپس

کد

و در نهایت

محصول نرم‌افزاری

تبدیل می‌شود.

---

# 2. Core Philosophy

## Software Factory Principle

در توسعه سنتی:

```text
Idea
  ↓
Developer
  ↓
Code
  ↓
Software
```

اما در AI Native Software Factory:

```text
Idea
  ↓
Knowledge Creation
  ↓
Specification
  ↓
AI Agents
  ↓
Implementation
  ↓
Validation
  ↓
Software Product
  ↓
Knowledge Evolution
```

اصل:

قبل از ساختن Software باید Brain آن ساخته شود.

---

# 3. Knowledge Architecture Overview

کل سیستم دانش سه لایه اصلی دارد:

```text
General Knowledge Layer
          ↓
Project Knowledge Layer
          ↓
Project Operating Memory
```

---

# 4. General Knowledge Layer

## Purpose

دانش عمومی و قابل استفاده مجدد برای تمام پروژه‌ها.

این لایه وابسته به یک پروژه خاص نیست.

شامل:

## Personal Preferences

Example:

**My Project Preferences**

شامل:

- Principles
- Rules
- Defaults
- Standards
- Technology Preferences

## Extended Knowledge

Example:

**My Project Extended Knowledge Preferences**

شامل:

- Patterns
- Practices
- Workflows
- Reusable Solutions
- Lessons Learned

## Framework Knowledge

شامل:

- Agentic SDLC Protocol
- AI Agent Rules
- Documentation Rules
- Quality Standards
- Governance Rules

---

# 5. Project Knowledge Layer

## Purpose

دانش اختصاصی هر پروژه.

این لایه هنگام شروع یک پروژه جدید ایجاد می‌شود.

مثال:

**ComputerJobs Project Knowledge**

شامل:

## Product Knowledge

- Vision
- Product Definition
- Product Principles
- Business Rules
- User Personas
- User Journeys

## UX Knowledge

شامل:

- UX Vision
- Design Principles
- Design System
- Component Patterns
- Content Principles

## Technical Knowledge

شامل:

- Architecture
- Technology Decisions
- Database Design
- API Design
- Security Principles

## Business Knowledge

شامل:

- Business Model
- Monetization
- Market Knowledge
- Competitive Analysis

---

# 6. Project Operating Memory (POM)

## Purpose

حافظه عملیاتی پروژه است.

POM باعث می‌شود پروژه Context خود را حفظ کند.

اصل:

> **Project Should Remember**

---

# 7. POM Structure

```text
Project Operating Memory
├── Project Knowledge Base
├── Project State Layer
├── Decision History
├── Execution History
└── Learning History
```

---

# 8. Project Knowledge Base

حافظه دانشی ثابت پروژه.

شامل:

- Vision
- Product Rules
- Architecture Principles
- Business Knowledge
- UX Knowledge
- Technical Knowledge

---

# 9. Project State Layer

حافظه وضعیت جاری پروژه.

Agent باید همیشه بداند:

- Current Phase
- Current Roadmap
- Current Task
- Completed Work
- Pending Work
- Blockers
- Next Actions

---

# 10. Decision History

تمام تصمیمات مهم ثبت می‌شوند.

شامل:

- ADRs
- Product Decisions
- Architecture Decisions
- Technology Decisions
- UX Decisions
- Trade-offs

هر تصمیم شامل:

- Context
- Problem
- Options
- Decision
- Benefits
- Risks
- Trade-offs

---

# 11. Execution History

ثبت فعالیت‌های اجرایی.

شامل:

- Tasks
- Specifications
- Reports
- Reviews
- Changes
- Releases

---

# 12. Learning History

تبدیل تجربه به دانش آینده.

شامل:

- Lessons Learned
- New Patterns
- Failed Approaches
- Improvements
- Recommendations

---

# 13. AI Agent Knowledge Flow

مدل استفاده Agentها از دانش:

```text
AI Agent
   ↓
Read General Knowledge
   ↓
Read Project Knowledge
   ↓
Read Project State
   ↓
Analyze Context
   ↓
Execute Task
   ↓
Generate Report
   ↓
Update Memory
```

---

# 14. AI Agent Roles

Software Factory شامل Agentهای تخصصی است:

```text
Orchestrator Agent
Product Agent
Architecture Agent
Documentation Agent
Engineering Agent
QA Agent
DevOps Agent
Security Agent
SEO Agent
```

هر Agent دارای:

- Role
- Goal
- Context
- Memory
- Tools
- Permissions
- Evaluation Criteria

---

# 15. AI Worker Pipeline

## Phase Zero: Knowledge Preparation

Responsible:

**Human + AI Assistant + AI Writer**

Output:

- Project Structure
- Anchor Documents
- Initial Knowledge Base

## Phase One: Documentation Development

Responsible:

**AI Documentation Developer**

Input:

- Anchor Documents
- SDLC Protocol
- Project Knowledge

Output:

- PRD
- SRS
- Architecture
- Specifications
- Detailed Documentation

## Phase Two: Software Development

Responsible:

**AI Developer**

Input:

- Approved Documentation
- Specifications
- Tasks
- State

Output:

- Code
- Tests
- Reports

---

# 16. Roadmap Ownership Model

Roadmapها توسط همان مرحله تولید می‌شوند.

## Master Roadmap

در ابتدای پروژه ایجاد می‌شود.

هدف:

نمای کلی پروژه.

## Phase Roadmap

توسط Agent مسئول همان Phase ایجاد می‌شود.

## Task Roadmap

برای اجرای فعالیت‌های جزئی ایجاد می‌شود.

اصل:

> هر مرحله مسئول طراحی مسیر اجرای خودش است.

---

# 17. State Update Protocol

بعد از هر Task:

```text
Before:
Read Current State

During:
Execute Task

After:
Validate Result
      ↓
Create Report
      ↓
Update State
      ↓
Update Knowledge If Needed
```

---

# 18. Source of Truth Model

ترتیب اعتبار:

```text
Anchor Documents
        ↓
Approved Documentation
        ↓
Decision Records
        ↓
Project State
        ↓
Task Records
        ↓
Source Code
```

---

# 19. Knowledge Evolution Cycle

دانش پروژه ثابت نیست.

چرخه:

```text
Experience
    ↓
Documentation
    ↓
Pattern
    ↓
Reusable Knowledge
    ↓
Future Projects
```

---

# 20. Final Goal

ایجاد یک AI Native Software Factory که:

- Context را حفظ می‌کند.
- تصمیمات گذشته را فراموش نمی‌کند.
- مستندات را خودکار تولید می‌کند.
- کیفیت را افزایش می‌دهد.
- وابستگی به انسان را کاهش می‌دهد.
- از تجربه پروژه‌ها یاد می‌گیرد.

نتیجه:

بدون Memory:

> AI فقط یک اجراکننده است.

با Memory:

> AI تبدیل به عضو دائمی تیم توسعه می‌شود.

---

**End of Document — Version 1.0**
