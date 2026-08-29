# EntityLens — Project Learning
## Version 1.0

This document captures the reusable project knowledge discovered and decided during the EntityLens project. It is intentionally stored in AiNote as project learning. It is not itself a Bootstrap contract; reviewed and generalized knowledge may later be promoted into a future Bootstrap version.

## 1. Product Identity

**EntityLens.ir** is an Entity Intelligence / Research service that receives the name of a person or company and researches publicly available information about that entity across the web and relevant social platforms.

The purpose is not merely search. The purpose is to build a rich, structured, evidence-linked understanding of an entity that can be consumed by AI and downstream products.

## 2. Product Form

EntityLens may exist as:

- an independent web application;
- an independent service/API;
- or both.

The service must therefore be usable independently while also serving other products through an API.

## 3. Primary Downstream Consumers

### AiWebSiteBuilder.ir

When a customer requests a website, EntityLens can first research the customer/person/company so that website generation is based on realistic information rather than invented sample data.

Potential inputs to website generation include:

- identity and basic information;
- current/previous website content;
- public web content;
- social profiles;
- contact information;
- email/contact details when publicly available;
- images;
- videos;
- business/activity information;
- brand information;
- logo and visual identity clues;
- colors and visual style clues;
- interests/preferences when publicly evidenced;
- other content useful for website copy and page generation.

### AiDrivenBusiness.ir

During business-transformation consulting, when a customer introduces themselves or their company, EntityLens can provide researched information that can be used as evidence/context for analysis and consulting documentation.

### ComputerJobs.ir

EntityLens can assist ComputerJobs in both sides of the marketplace:

**Job seeker:**
- profile enrichment;
- resume drafting/enrichment;
- extraction of publicly evidenced professional background and activities;
- professional content assistance.

**Employer/company:**
- company information enrichment;
- employer profile completion;
- job-posting content assistance;
- research about the company and its public presence.

### Future Products

The EntityLens API is intended to be reusable by additional products in the ecosystem in the future.

## 4. Core User Interaction

The intended initial UI is login-protected.

The main interaction is a search/research box where the user enters a person or company name and activates Search. The system then produces structured, categorized results containing multiple media/data types.

Conceptual flow:

```text
Login
  ↓
Entity name/input
  ↓
Search / Research
  ↓
Web + Social discovery
  ↓
Entity resolution / disambiguation
  ↓
Evidence-linked normalization
  ↓
Categorized entity profile
  ↓
API / downstream AI consumption
```

The exact information architecture of the result screen is not yet a final frozen contract.

## 5. Data Types

EntityLens should be able to collect and organize multiple data types, including:

- text;
- images/photos;
- videos;
- links;
- websites;
- social profiles;
- contact information;
- brand information;
- professional/business activity information;
- other relevant publicly available entity data.

## 6. Research Sources

Research is intended to cover:

- the public web;
- official websites;
- social networks/platforms;
- other relevant public sources.

The system should preserve source/evidence relationships rather than producing unsupported facts.

## 7. Entity Resolution and Disambiguation

This is a critical product requirement discovered during the project.

### Aliases / Pseudonyms

A person may appear online under:

- a real name;
- nickname;
- pseudonym;
- alias;
- username/handle;
- other known names.

Entity research should therefore consider identity variants rather than relying only on exact-name matching.

### Same Name, Different People

Multiple people can share the same first/last name while working in unrelated fields. EntityLens must not automatically merge all matching search results into one entity.

Conceptual requirement:

```text
Name
 ↓
Candidate identities
 ↓
Context / field / source correlation
 ↓
Disambiguated entity or multiple possible entities
```

Entity resolution must be treated as a first-class concern.

## 8. Evidence and Source Traceability

Research output should be traceable to its sources.

Conceptual relationship:

```text
Claim / Data
  ↓
Source
  ↓
URL / Platform
  ↓
Evidence
```

This is important both for trust and for downstream AI systems that need to distinguish sourced information from inference.

## 9. Context Package for AI Product Generation

A key strategic purpose of EntityLens is to turn entity research into a reusable context package for AI agents.

Conceptual flow:

```text
Entity
 ↓
Research
 ↓
Normalized structured data
 ↓
Evidence / sources
 ↓
Entity context package
 ↓
AI product generation / assistance
```

The package can provide downstream agents with realistic information about the person/company instead of forcing the agent to invent details.

## 10. Brand and Content Intelligence

Entity research may support downstream generation/analysis of:

- website copy;
- email/content drafting;
- contact details;
- logo-related inputs or logo research;
- color palette clues;
- visual identity clues;
- page/content structure;
- tone/style clues;
- other brand-related website inputs.

These are intended uses of researched evidence; they are not yet frozen implementation specifications.

## 11. Ecosystem Position

Conceptual ecosystem:

```text
                         EntityLens
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                 │
 AiWebSiteBuilder      ComputerJobs    AiDrivenBusiness
          │                 │                 │
   Website generation  Career/job help   Business consulting

                         EntityLens API
                              │
                     Future ecosystem products
```

EntityLens is therefore best understood as shared entity-intelligence infrastructure rather than a feature belonging exclusively to one product.

## 12. Agentic SDLC / Documentation Learning

A major process lesson discovered while building EntityLens is that Foundation Approval must be a durable transition in the repository.

Before Foundation Approval, the project remains in discovery/foundation work and agents must not prematurely assume the full documentation lifecycle.

After Foundation Approval, a replacement Documentation Agent (regardless of model/provider) must be able to continue the project's documentation lifecycle from the repository alone.

The Documentation Agent should:

- read the repository state;
- read the approved Foundation documentation;
- derive the required documentation sequence from the project's SDLC/protocol/registry/artifact graph/state/gates;
- create the remaining required documentation artifacts;
- continue until Documentation Readiness;
- not depend on the previous agent's chat history;
- preserve durable project knowledge in repository artifacts.

This requirement is agent/model/provider independent. DeepSeek is one possible Documentation Agent; the behavior must not depend on DeepSeek specifically.

## 13. Project Knowledge Must Not Live Only in Chat

Critical principle discovered during the project:

> No knowledge that is necessary to continue the project may exist only in Chat.

If a discovery, decision, constraint, requirement, or learning is necessary for continuation, it must be represented in durable project artifacts.

## 14. Knowledge Loop Position

The agreed Knowledge Loop is:

```text
Project execution
  ↓
Project learning / discoveries
  ↓
AiNote
  ↓
Review / Generalize
  ↓
Bootstrap next version
  ↓
Future project
```

AiNote is passive during normal project execution: it is the upstream knowledge laboratory and receives project learning rather than acting as an active dependency that controls the project's execution.

Only reviewed/generalized knowledge should influence a future Bootstrap version.

This follows the current canonical knowledge map: AiNote is the upstream Knowledge Laboratory, Bootstrap is the curated executable baseline, and project learning returns to AiNote for governed promotion. 

## 15. Bootstrap Promotion Boundary

EntityLens-specific implementation decisions should not automatically become Bootstrap rules.

The appropriate boundary is:

```text
EntityLens discovery
 ↓
Project learning captured here
 ↓
Review / generalization
 ↓
Candidate for Bootstrap
 ↓
Approved Bootstrap vNext
```

The purpose of this document is therefore to preserve the project learning so it can be reviewed and generalized later.

## 16. Important Reusable Lessons

1. Entity research requires entity resolution, not simple name search.
2. Aliases, pseudonyms and usernames must be considered.
3. Same-name people/companies must be disambiguated.
4. Research claims need source/evidence traceability.
5. Entity intelligence becomes more valuable when packaged for downstream AI agents.
6. A shared Entity Intelligence API can serve multiple products.
7. EntityLens should be usable independently and as infrastructure.
8. Website generation benefits from realistic researched context instead of invented sample data.
9. Foundation Approval must be a durable repository state transition.
10. After Foundation Approval, Documentation Agent behavior must be independent of the previous agent/model/provider.
11. No essential continuation knowledge should remain only in Chat.
12. Project learning should return to AiNote and only reviewed/generalized knowledge should influence future Bootstrap versions.

**End — EntityLens Project Learning v1.0**
