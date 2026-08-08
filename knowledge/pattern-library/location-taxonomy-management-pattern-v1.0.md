# Location & Taxonomy Management Pattern

## Version 1.0

---

# 1. Purpose

این Pattern برای مدیریت داده‌های طبقه‌بندی‌شده مانند:

- Location
- Category
- Taxonomy
- Skills
- Industries

طراحی شده است.

هدف:

ایجاد ساختار قابل توسعه، قابل مدیریت و قابل استفاده توسط انسان و AI.

---

# 2. Core Principles

Location و Taxonomy نباید Hard Code باشند.

تمام داده‌ها باید:

- Database Driven
- Admin Managed
- Extendable
- Searchable
- AI Ready

باشند.

---

# 3. Location Hierarchy

Default hierarchy:

```text
Country
  ↓
Province / State
  ↓
City
```

Example:

```text
Iran
  ↓
Tehran Province
  ↓
Tehran City
```

---

# 4. Location Entity Rules

Location باید موجودیت مستقل باشد.

مدیریت توسط Admin:

Admin can:

- Create Province
- Edit Province
- Disable Province
- Create City
- Edit City
- Disable City
- Approve Suggested Locations

---

# 5. User Location Suggestion Workflow

Users can suggest missing locations.

Example:

User selects:

Province:
Tehran

Suggests:

City:
Example New City

Workflow:

```text
User Suggestion
      ↓
Pending Review
      ↓
Admin Review
      ↓
Approve / Reject
```

If Approved:

Location becomes available for all users.

If Rejected:

Suggestion remains archived.

---

# 6. Suggestion Data Model

Location Suggestion should store:

- Suggested Name
- Parent Location
- Suggested By User
- Creation Date
- Status
- Admin Note
- Approval Date

Status:

```text
Pending
  ↓
Approved
  ↓
Rejected
```

---

# 7. Permission Rules

Normal Users:

Can:

- View locations
- Suggest new locations

Cannot:

- Directly create official locations

Admin:

Can:

- Approve
- Reject
- Modify
- Merge duplicates

---

# 8. Duplicate Prevention

Before approval:

System should check:

- Existing name
- Similar names
- Alternative spellings
- Aliases

Example:

```text
تهران
Tehran
```

should not create duplicates.

---

# 9. SEO Considerations

Locations should support:

- SEO Pages
- Friendly URLs
- Metadata
- Aliases

Example:

```text
/jobs/tehran
/jobs/shiraz
```

---

# 10. AI & Knowledge Integration

Location data should be usable by:

- AI Assistant
- AI Agents
- Search Engine
- Recommendation Engine
- RAG System

Example:

AI Mentor:

> "برای موقعیت شغلی React Developer، شهر تهران گزینه‌های بیشتری دارد."

---

# 11. Taxonomy Extension

The same pattern applies to:

```text
Category
  ↓
SubCategory
  ↓
Skill
  ↓
Technology
```

Example:

```text
Software Development
  ↓
Frontend
  ↓
React Developer
  ↓
Next.js
```

---

# 12. Future Extensions

Possible future features:

- Popularity Ranking
- User Voting
- AI Suggested Locations
- Automatic Data Cleaning
- Geographic Search
- Map Integration

---

# 13. Design Principles

Follow:

- Domain Driven Design Ready
- Event Driven Ready
- Knowledge Base First
- Admin Controlled
- User Assisted Growth

---

# Final Goal

Create a living taxonomy system that improves continuously through:

Users

+

Administrators

+

AI Systems

---

**End of Pattern — Version 1.0**
