# Infomatics v2 — Project Plan

**Version:** v1.0  
**Date:** 2026-07-19  
**Status:** Phase 0 — Project Initialization  
**Repository:** [rwnq8/infomatics-v2](https://github.com/rwnq8/infomatics-v2)

---

## §0. Why v2 — What v1 Got Wrong

Infomatics v1 (rwnq8/infomatics, deprecated) made three fundamental errors:

1. **Numerology disguised as derivation.** Claimed α ≈ 1/137 because "p=137 is prime." This is Eddington-style numerology — the exact pattern QNFO's own Cross-Ratio paper identifies as post-hoc curve fitting.

2. **LLM-recalled citations.** Most bibliography entries were generated from training data, never verified against actual papers. External literature was claimed but never systematically searched.

3. **QNFO self-referential loop.** Claims were supported by QNFO papers that cite other QNFO papers, with zero external validation. The p-adic/Bruhat-Tits/ZBW connection has no peer-reviewed support outside the QNFO ecosystem.

**v2 reframes the project as an evidence-based literature survey.** We audit claims, not make them. We classify, not derive.

---

## §1. Charter

### 1.1 Mission

> **Systematically audit claims about "information as fundamental substrate" across QNFO-internal and external physics literature. Classify every claim by evidential support using a transparent, reproducible rubric. Produce an honest map of what's established, what's speculative, and what's disconfirmed.**

### 1.2 Core Question

> What is the evidential status of the claim that "information is the fundamental substrate of physical reality, with matter, energy, space, and time emerging from information-theoretic constraints"?

### 1.3 Governing Rules

| Rule | Description |
|:-----|:------------|
| **No LLM-recalled citations** | Every bibliography entry must be verified against an actual source (arXiv API, Semantic Scholar API, DOI resolution, publisher page) |
| **External sources first** | QNFO-internal papers are cross-referenced, not used as primary evidence for claims about physics |
| **Honest classification** | Every claim receives one of five transparent tags (see §3) |
| **Falsifiability required** | Any claim presented as physics must have a stated condition under which it would be false |
| **No numerology** | Numerical coincidences (137 is prime, 1/α ≈ 137) are noted as coincidences, not presented as derivations |

---

## §2. Scope

### 2.1 Claims Under Audit

The project audits claims in these domains:

| Domain | Key Question | Representative Claims |
|:-------|:-------------|:----------------------|
| **D1: Wheeler's "It from Bit"** | Is "information is fundamental" a testable hypothesis? | Wheeler 1989, Vedral 2010, Lloyd 2006 |
| **D2: Zitterbewegung physics** | What is the experimental status of ZBW? | Dirac 1928, Gerritsma 2010, Brusheim & Xu 2008 |
| **D3: α as geometric ratio** | Is α = r_e/λ_C a novel insight or the standard definition? | Sommerfeld 1916, QNFO Cross-Ratio paper, CODATA |
| **D4: Electron structure** | Does the electron have measurable internal structure? | LEP constraints, classical vs. QFT electron |
| **D5: p-adic/ultrametric connection** | Is there experimental evidence for p-adic structure in physics? | QNFO ZBW-Majorana P1-P7, Dragovich et al. 2009 |
| **D6: Adelic framework** | Has the adelic Dirac equation made testable predictions? | QNFO Grand Synthesis P7, external literature |
| **D7: Information-theoretic QFT** | Can QFT be derived from information axioms? | Chiribella et al. 2011, 2021, Hardy 2001 |

### 2.2 Out of Scope

- **Deriving** α or any physical constant (this is classification, not derivation)
- **Axiomatic framework** construction (v1's error; v2 catalogs existing frameworks, doesn't create new ones)
- **QNFO-internal-only claims** unless they are clearly flagged as such
- **Generating new physics hypotheses** (the deliverable is a MAP, not a theory)

---

## §3. Evidence Classification System

Every claim receives exactly one tag:

| Tag | Definition | Example |
|:----|:-----------|:--------|
| **[Established]** | Supported by peer-reviewed experimental evidence and/or mathematical theorems with consensus | α = e²/(ħc) ≈ 1/137.036; Dirac equation predicts ZBW mathematically |
| **[Open]** | Active research question with competing hypotheses, no experimental consensus | Does ZBW exist for free electrons? Is electron structure below 10⁻¹⁸ m? |
| **[Speculative]** | Theoretical proposal without experimental evidence or peer-reviewed confirmation | p-adic observable for ZBW; adelic Dirac equation; cross-ratio reframing of α |
| **[Disconfirmed]** | Contradicted by experimental evidence or established theorems | Eddington's α⁻¹ = 136 numerology; classical electron radius as physical size |
| **[QNFO-Internal]** | Exists only within the QNFO ecosystem; no external citations, peer review, or experimental validation | ZBW→Bruhat-Tits trees; Ostrowski-based QEC; α-π-Helix vortex model |

---

## §4. Search Methodology

### 4.1 External Sources (Primary)

| Source | Method | Frequency |
|:-------|:-------|:----------|
| **arXiv API** | Keyword search via `export.arxiv.org/api/query`, max_results=10 per query, sortBy=relevance | Per claim domain |
| **Semantic Scholar API** | `/graph/v1/paper/search` with citation-weighted relevance | Per claim domain |
| **INSPIRE-HEP** | High-energy physics database with citation tracking | For QFT/particle physics claims |
| **Publisher APIs** | DOI resolution via crossref.org, publisher page verification | Per citation |
| **Web search** | Google Scholar, journal pages for verification | As needed |

### 4.2 QNFO Sources (Cross-Reference)

| Source | Purpose |
|:-------|:--------|
| **QNFO Knowledge Graph** | Identify internal papers on topic; count external citations |
| **QNFO D1 living-paper** | Check for internal papers with DOIs; cross-reference against external citations |
| **QNFO Vectorize** | Semantic search for internal papers overlapping with external work |
| **QNFO Working Memory** | Context for project history; not used as evidence |

### 4.3 Citation Standards

- Every cited paper must have: author(s), year, title, and a resolvable identifier (DOI, arXiv ID, or journal reference)
- "Private communication" and "QNFO internal" may be cited only as context, never as evidence
- Every claim must cite at least one external (non-QNFO) source

---

## §5. Work Breakdown Structure

| Phase | Tasks | Deliverable | Duration |
|:------|:------|:------------|:---------|
| **0: Init** | 0.1 Repo + scaffold, 0.2 Project plan, 0.3 Classification rubric, 0.4 Search test, 0.5 Closeout | Git tag v0.1-phase0 | 1 day |
| **1: External Search** | 1.1 D1 (It from Bit), 1.2 D2 (ZBW), 1.3 D3 (α ratio), 1.4 D4 (Electron structure), 1.5 D5 (p-adic), 1.6 D6 (Adelic), 1.7 D7 (Info-QFT) | 7 domain search reports with verified citations | 5 days |
| **2: QNFO Audit** | 2.1 KG cross-reference, 2.2 D1 paper audit, 2.3 Vectorize semantic overlap, 2.4 Internal citation tracking | QNFO due diligence report | 3 days |
| **3: Classification** | 3.1 Evidence matrix, 3.2 Domain verdicts, 3.3 Gap analysis | Classification matrix | 3 days |
| **4: Synthesis** | 4.1 Consolidated report, 4.2 Zenodo publication, 4.3 D1 + papers-server deploy | Published paper with DOI | 3 days |

---

## §6. Milestones

| Milestone | Gate Criteria |
|:----------|:--------------|
| **M0: Project Initialized** | Git repo on feature branch, PROJECT-PLAN.md written, classification rubric defined, search methodology documented |
| **M1: External Search Complete** | 7 domain reports with ≥5 verified external citations each, 0 LLM-recalled citations |
| **M2: QNFO Audit Complete** | All internal papers classified with external citation counts, overlap map with external literature |
| **M3: Classification Matrix** | Every claim in all 7 domains receives one of 5 tags with external evidence justification |
| **M4: Published** | Consolidated paper on Zenodo with DOI, D1 living-paper, papers.qnfo.org |

---

## §7. Risk Register

| Risk | Likelihood | Impact | Mitigation |
|:-----|:-----------|:-------|:-----------|
| **R1: Rate-limiting on external APIs** | Medium | Medium | Cache results; stagger queries; prioritize arXiv over S2 if rate-limited |
| **R2: QNFO-internal claims unverifiable externally** | High | Low | Tag as [QNFO-Internal]; this is a finding, not a failure |
| **R3: Project scope exceeds available evidence** | Medium | Medium | Narrow scope to domains with literature; document empty domains as gaps |
| **R4: LLM recall contaminates bibliography** | Medium | High | MANDATORY: every citation verified against API or DOI before inclusion |
| **R5: Git race condition (v1 incident)** | Medium | High | ALL git operations from persistent directory; NEVER temp-dir batch git with cleanup |
| **R6: Previous v1 content contaminates v2** | Low | Medium | Explicit v1/v2 separation; different repo; clearly marked deprecation |

---

## §8. Deliverable Registry

| Deliverable | Path | Format | Phase |
|:------------|:-----|:-------|:------|
| Project charter | PROJECT-PLAN.md | Markdown | 0 |
| Risk register | RISK-REGISTER.md | Markdown | 0 |
| Deliverable registry | DELIVERABLE-REGISTRY.md | Markdown | 0 |
| Classification rubric | notebooks/rubric.md | Markdown | 0 |
| D1–D7 search reports | artifacts/d{1-7}-*.md | Markdown | 1 |
| QNFO due diligence report | artifacts/qnfo-due-diligence.md | Markdown | 2 |
| Evidence classification matrix | artifacts/classification-matrix.md | Markdown | 3 |
| Consolidated survey paper | releases/infomatics-v2-survey.md | Markdown + PDF | 4 |

---

## §9. Version History

| Version | Date | Description | Git Tag |
|:--------|:-----|:------------|:--------|
| 0.1 | 2026-07-19 | Project initialization | v0.1-phase0 |
