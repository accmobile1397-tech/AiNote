# AI-Native Project Bootstrap & Agent-Independent Memory Pattern

**Version 1.0**

## 1. Purpose

این Pattern استاندارد شروع هر پروژه AI-native است.

هدف آن این است که پروژه از **اولین Task** دارای یک حافظه عملیاتی مستقل از:

- Chat
- AI Model
- AI Agent
- AI Writer
- Documentation Developer
- Coding Developer
- IDE
- Human Session

باشد.

اصل بنیادی:

> **Project Memory must outlive every Agent, Model, Tool, and Conversation.**

---

# 2. Governing Memory Architecture

هر پروژه باید از همان ابتدای کار، معماری:

**AI Native Project Operating Memory (POM)**

را ایجاد و Initialize کند.

POM شامل:

```text
01. Project Knowledge Base
02. Project State Layer
03. Decision History
04. Execution History
05. Learning History
```

است.

POM جایگزین Documentation نیست.

POM، سیستم مدیریت چرخه حیات دانش و وضعیت پروژه است.

---

# 3. First Task Rule

اولین Task هر پروژه باید:

**TASK-0001 — Project Bootstrap & POM Initialization**

باشد.

TASK-0001 نباید Coding باشد.

TASK-0001 باید:

1. Project Context را تثبیت کند.
2. POM را Initialize کند.
3. Project State را ایجاد کند.
4. Master Roadmap را ایجاد کند.
5. Current Objective را ثبت کند.
6. Current Task را ثبت کند.
7. Known Decisions را ثبت یا Reference کند.
8. Next Task را مشخص کند.
9. Agent Independence را برقرار کند.

---

# 4. Project State Must Exist From Day One

Project State باید از همان اولین Task مشخص کند:

```text
Project
Current Phase
Current Milestone
Current Task
Current Objective
Completed Work
Current Work
Pending Work
Blockers
Next Actions
```

بنابراین پروژه حتی بدون Chat History قابل ادامه باشد.

---

# 5. Master Roadmap

در Bootstrap یک **Master Project Roadmap** ایجاد شود.

Master Roadmap فقط Lifecycle کلی پروژه را مشخص کند.

مثلاً:

```text
Phase 0 — Foundation
Phase 1 — MVP
Phase 2 — Expansion
Phase 3 — Scale
...
```

جزئیات Phaseهای آینده نباید زودهنگام ساخته شوند.

---

# 6. Phase Ownership Rule

هر Phase توسط Agent مسئول همان Phase برنامه‌ریزی می‌شود.

مدل:

```text
Phase Start
    ↓
Read POM
    ↓
Read Previous State
    ↓
Analyze Inputs
    ↓
Create Phase Roadmap
    ↓
Create Phase Tasks
    ↓
Execute
```

بنابراین:

**Master Roadmap = High-Level**

و:

**Phase Roadmap = Detailed**

---

# 7. Foundation Must Have Its Own Roadmap

بعد از Bootstrap، Task بعدی باید:

**TASK-0002 — Foundation Planning**

باشد.

Foundation Planning باید:

- Foundation Scope
- Foundation Documents
- Document Dependencies
- Foundation Tasks
- Completion Criteria
- Validation Rules
- Foundation Freeze Criteria

را مشخص کند.

---

# 8. Foundation Roadmap Must Become Project Memory

Foundation Roadmap نباید فقط در ذهن Agent یا Chat باقی بماند.

باید در POM ثبت شود.

بنابراین پروژه همیشه بداند:

```text
Foundation
│
├── Document A ✅
├── Document B ✅
├── Document C ⏳
├── Document D ⏳
│
└── Next Task
```

و وضعیت هر Task در Project State / Execution History ثبت شود.

---

# 9. Agent Independence Rule

هیچ Task نباید به یک Agent خاص وابسته باشد.

اگر Task توسط:

```text
AI Writer
```

شروع شد، باید بتواند توسط:

```text
Claude
ChatGPT
Gemini
Documentation Developer
Human
Future Agent
```

ادامه پیدا کند.

Agent فقط Executor است.

**POM مالک Context پروژه است.**

---

# 10. Agent Context Recovery

هر Agent جدید باید بتواند بدون Conversation قبلی پروژه را بازیابی کند.

حداقل Context:

```text
PROJECT CONTEXT
+
PROJECT STATE
+
KNOWLEDGE INDEX
+
CURRENT TASK
+
RELEVANT DECISIONS
+
RELEVANT DOCUMENTATION
```

Agent نباید از Human بخواهد:

> «قبلاً چه کار کرده بودیم؟»

بلکه باید Project Memory را بخواند.

---

# 11. Task Contract

هر Task باید حداقل داشته باشد:

```text
Task ID
Title
Objective
Inputs
Required Knowledge
Constraints
Dependencies
Expected Outputs
Acceptance Criteria
Status
Owner
Artifacts
Execution Report
```

بنابراین Agent جدید می‌تواند Task را مستقل اجرا کند.

---

# 12. Universal Task Lifecycle

تمام Agentها از این چرخه استفاده کنند:

```text
READ
 ↓
UNDERSTAND
 ↓
EXECUTE
 ↓
VALIDATE
 ↓
REPORT
 ↓
UPDATE POM
 ↓
CONTINUE
```

Agent موظف است بعد از اجرای Task، Memory پروژه را به‌روزرسانی کند.

---

# 13. Agent Handoff Rule

تحویل کار بین Agentها باید از طریق Project Memory انجام شود.

مثال:

```text
AI Writer
    ↓
POM Update
    ↓
Claude
    ↓
POM Update
    ↓
Documentation Developer
    ↓
POM Update
    ↓
Coding Developer
```

نه از طریق:

```text
Chat History
```

---

# 14. Foundation Workflow

Foundation باید به این ترتیب پیش برود:

```text
TASK-0001
Project Bootstrap
      ↓
POM Initialization
      ↓
TASK-0002
Foundation Planning
      ↓
Foundation Roadmap
      ↓
Foundation Tasks
      ↓
Foundation Documents
      ↓
Foundation Validation
      ↓
Foundation Freeze
```

---

# 15. Foundation Agent Independence

Foundation نباید به AI Writer وابسته باشد.

AI Writer ممکن است نویسنده Foundation باشد، اما Project باید بتواند Foundation را با Agent دیگری ادامه دهد.

مثلاً:

```text
Foundation Document 1
       ↓
AI Writer

Foundation Document 2
       ↓
AI Writer

Foundation Document 3
       ↓
Claude

Foundation Document 4
       ↓
Human / Documentation Developer
```

تا زمانی که POM و Task State صحیح باشند، هیچ مشکلی وجود ندارد.

---

# 16. Source of Truth

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

Chat History منبع حقیقت پروژه نیست.

Agent Memory منبع حقیقت پروژه نیست.

---

# 17. Decision Persistence

هر تصمیم مهم باید از Conversation خارج و در Project Memory ثبت شود.

موارد شامل:

- Product Decisions
- Architecture Decisions
- Technology Decisions
- UX Decisions
- Business Decisions
- Trade-offs

هیچ تصمیم مهمی نباید فقط در Chat باقی بماند.

---

# 18. Learning Persistence

تجربیات مهم نیز باید در POM ثبت شوند:

```text
Lessons Learned
Patterns Discovered
Failed Approaches
Improvements
Future Recommendations
```

هدف این است که پروژه از اجرای خودش یاد بگیرد.

---

# 19. Agent Replacement Test

یک پروژه زمانی این Pattern را به‌درستی اجرا کرده است که بتوان:

1. Chat فعلی را ببندیم.
2. Agent فعلی را حذف کنیم.
3. Agent جدید وارد کنیم.
4. POM را به او بدهیم.
5. Agent بدون توضیح دستی پروژه را ادامه دهد.

اگر این اتفاق ممکن نباشد، Project Memory ناقص است.

---

# 20. Project Continuity Test

قبل از پایان هر Major Task باید بتوان پاسخ این سؤال‌ها را فقط از Repository داد:

```text
What is the project?
Why are we building it?
Where are we?
What has been completed?
What is currently being done?
What decisions have been made?
What remains?
What is the next task?
Who/what is responsible?
What documents are authoritative?
```

---

# 21. No Hidden Context Rule

هیچ Context حیاتی نباید فقط در:

```text
Human Memory
ChatGPT Memory
AI Writer Memory
Claude Memory
Cursor Session
Slack / Chat
```

باقی بماند.

اگر Context برای ادامه پروژه لازم است:

> **Persist it in Project Memory.**

---

# 22. Bootstrap Output

در پایان TASK-0001 پروژه باید حداقل این وضعیت را داشته باشد:

```text
POM
├── Project Knowledge Base
├── Project State Layer
├── Decision History
├── Execution History
└── Learning History

Master Project Roadmap

Current Task

Next Task
```

---

# 23. Universal Next-Step Rule

پس از Bootstrap:

```text
POM
 ↓
Current State
 ↓
Current Phase
 ↓
Phase Roadmap
 ↓
Current Task
 ↓
Required Skill
 ↓
Responsible Agent
 ↓
Artifact
 ↓
Validation
 ↓
POM Update
 ↓
Next Task
```

بنابراین پروژه باید بتواند **خودش مسیر بعدی را مشخص کند.**

---

# 24. Core Principle

هدف این Pattern این نیست که:

> AI Writer پروژه را به خاطر بسپارد.

هدف این است که:

> **Project خودش را به خاطر بسپارد.**

بنابراین:

```text
Agent = Replaceable
Model = Replaceable
Tool = Replaceable
Chat = Replaceable

POM = Persistent
Project Knowledge = Persistent
Project State = Persistent
Decisions = Persistent
```

---

# 25. Reusable Instruction

هر زمان این Pattern به ChatGPT داده شد، ChatGPT باید:

1. آن را به‌عنوان **Project Bootstrap Pattern** در نظر بگیرد.
2. قبل از شروع substantive project work، POM را ایجاد/بررسی کند.
3. TASK-0001 را Bootstrap + POM Initialization قرار دهد.
4. Master Roadmap را ایجاد کند.
5. Foundation Planning را به TASK-0002 تبدیل کند.
6. Foundation Roadmap را در POM ثبت کند.
7. هیچ Agent خاصی را مالک حافظه پروژه نکند.
8. تمام تصمیمات مهم را از Chat به Project Memory منتقل کند.
9. وضعیت پروژه را پس از Taskها به‌روزرسانی کند.
10. اطمینان حاصل کند که Agent دیگری بتواند بدون Conversation قبلی پروژه را ادامه دهد.

---

## Final Rule

> **Never start an AI-native project by relying on conversation memory. Bootstrap the Project Operating Memory first, then let agents operate on top of it.**

**End of Pattern — Version 1.0**
