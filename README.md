# Understanding AI Data Production & Community Impacts Worldwide: A Multivocal Literature Review

**Companion repository for the ACM RC journal submission:**
*"Understanding AI Data Production & Community Impacts Worldwide: A Multivocal Literature Review"*

Anonymous Author(s)

This repository contains the coded dataset and supplementary visualizations regarding the search and selection protocol used in our Multivocal Literature Review (MLR).

| **Paper** | **Dataset** | **Appendices** |
|---|---|---|
| [**Read Draft (PDF)**](docs/multivocal-ai-data-communities.pdf) | [**MLR Corpus (Excel)**](data/mlr_corpus_350.xlsx) | [**Supplementary Appendices (PDF)**](docs/supplementary-appendices.pdf) |

---

## Search & Selection Process

The following flow diagram details our attrition and selection protocol, integrating representative academic searches (ACM) with grey literature strategies.

> **Note:** This figure supplements the methodology section of the submitted PDF.

```mermaid
flowchart TD
 %% --- STYLES ---
 classDef prep fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#000;
 classDef acm fill:#e3f2fd,stroke:#1565c0,stroke-width:2px,color:#000;
 classDef grey fill:#fff3e0,stroke:#e65100,stroke-width:2px,color:#000;
 classDef final fill:#e8f5e9,stroke:#2e7d32,stroke-width:3px,color:#000;
 classDef titleNode fill:none,stroke:none,font-weight:bold,font-size:16px,color:#000;

 %% --- PHASE 0 ---
 subgraph Prep ["PHASE 0: PROTOCOL REFINEMENT (Aug-Sept 2024)"]
 direction TB
 P1["A/D/C Framework Dev<br/>& Keyword Strategy"]:::prep
 P2["Pilot Searches<br/>Tested against known<br/>seminal papers"]:::prep
 P1 --> P2
 end

 %% --- PHASE 1 ---
 subgraph ACMFlow [" "]
 direction TB
 Title1["PHASE 1: REPRESENTATIVE SEARCH (ACM)"]:::titleNode

 A1[("ACM Digital Library<br/>(Primary Query Sets)")]:::acm
 A2["Identification<br/>Hits: 1,914"]:::acm
 A3["Screening<br/>(Title/Abstract)<br/>Screened: 1,201"]:::acm
 A4["Eligibility<br/>(Full Text A/D/C)<br/>Met Criteria: 153"]:::acm
 A5["Included<br/>Unique Sources: 48"]:::acm

 Title1 --> A1
 A1 --> A2 --> A3 --> A4 --> A5
 end

 %% --- PHASE 2 ---
 subgraph OtherStreams ["PHASE 2: EXPANDED SEARCH (Aug 2024 - Jan 2025)"]
 direction TB
 B1[("Other Academic DBs<br/>IEEE, ScienceDirect, Springer,<br/>Wiley, Taylor & Francis")]:::acm

 C1[("Grey Literature<br/>Org Reports, Policy Docs,<br/>Google Search")]:::grey

 C2[("Targeted Hand-Search<br/>CHI, FAccT, CSCW, JRC,<br/>Big Data & Society, AI & Soc")]:::grey

 Process["Rigorous Consensus Review<br/>-----------------------------<br/>• Two authors lead screening<br/>• Batched presentation to full team<br/>• 2 Rounds (Aug-Sept 2024)<br/>• Team iteration through Jan 2025"]:::prep
 end

 %% --- FINAL CORPUS ---
 FinalBox["FINAL CORPUS (N = 350)<br/>---------------------------------------<br/>Database Searches: 174 (50%)<br/>Existing Networks/Orgs: 73 (21%)<br/>Citation Snowballing: 51 (15%)<br/>Iterative Keyword Search: 31 (9%)<br/>Hand-Searching Journals: 21 (6%)"]:::final

 %% --- CONNECTIONS ---
 P2 --> Title1
 P2 --> B1

 A5 --> FinalBox
 B1 --> Process
 C1 --> Process
 C2 --> Process
 Process --> FinalBox
```

---

## Context: The AI Development Pipeline

We position data production not as a mere prerequisite, but as a site of sociotechnical power. The image below illustrates the interwoven domains of AI (A), Data Production (D), and Community Impacts (C).

![AI development pipeline](docs/assets/pipe2.jpg)
