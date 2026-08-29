# LC-0006 — EntityLens → ComputerJobs Entity Intelligence

## Source

EntityLens project discovery.

## Status

candidate — pending review/generalization

## Observation

EntityLens can act as a shared Entity Intelligence layer for ComputerJobs.ir, in addition to AiWebSiteBuilder.ir and AiDrivenBusiness.ir.

The same underlying research about an entity should be reusable by multiple products rather than repeatedly collected and reconstructed inside each product.

## Candidate Applications

### Candidate Intelligence

For a job seeker, EntityLens may provide evidence-backed public context that helps ComputerJobs with:

- candidate/profile enrichment
- professional identity context
- public work history signals
- skills and technology signals
- projects and public evidence
- GitHub / LinkedIn / personal-site context where publicly accessible and appropriately matched
- resume assistance
- cover-letter assistance

### Company Intelligence

For an employer, EntityLens may provide public company context for:

- company profile enrichment
- company description
- products/services
- public digital presence
- brand signals
- relevant public people
- public contact information
- content and media references

### Job Posting Assistance

ComputerJobs may combine Company Intelligence with employer-provided job requirements to assist with:

- job description generation/improvement
- responsibilities
- required skills
- preferred skills
- company context
- tone and positioning
- benefits/context where supported

## Candidate Generalization

> A shared Entity Intelligence layer can provide reusable, evidence-backed context to multiple products while product-specific applications remain in each consuming product's domain.

```text
                         EntityLens
                             │
          ┌──────────────────┼──────────────────┐
          ↓                  ↓                  ↓
   ComputerJobs      AiWebSiteBuilder   AiDrivenBusiness
          │
     ┌────┴────┐
     ↓         ↓
 Candidate   Company
 Intelligence Intelligence
     │         │
 Resume      Profile
 Cover       Job Posting
 Letter      Assistance
```

## Architectural Implication

EntityLens should remain responsible for canonical Entity Intelligence, provenance, uncertainty, and evidence. Resume generation, job-posting logic, candidate workflows, and business-domain recommendations remain responsibilities of consuming products.

## Reusability Assessment

- Reusable beyond EntityLens: yes
- Cross-product architecture pattern: yes
- Product-specific implementation details: no
- Domain-specific: partially; the shared-layer principle is generalizable
- AI-agent design implications: yes
- Requires product/market validation: yes
- Requires human/product-owner review before canonicalization: yes

## Governance

This is an intake candidate, not canonical knowledge. It must be reviewed, challenged, generalized, and validated before promotion into the Pattern Library, project preferences, Bootstrap, or any product-specific source of truth.

No project should inherit this candidate automatically merely because it appears here.
