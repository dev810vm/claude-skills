# Reference Files Changelog

Tracks methodology and content changes to the reference files in this directory. Most recent changes first.

---

## 2026-03-26 — Deep research validation pass

**Files:** `ai-screening-research.md`, `scoring-rubric.md`
**Trigger:** Full validation of all claims against current sources (47 claims checked, 31 confirmed, 4 corrected)

### ai-screening-research.md

| Change | Old | New | Reason |
|---|---|---|---|
| Workday + Paradox acquisition status | "announced 2025, pending close" | "closed October 1, 2025" | Acquisition completed; source: Workday Newsroom Oct 1 2025 |
| HireVue optimal response length | "Target 90–120 seconds per answer" | "Target 60–90 seconds delivery; employer limit is 90–120 seconds" | Coaching sources consistently cite 60–90s as optimal delivery, distinct from the employer-set time window |
| Stanford age bias study framing | "gave older male candidates higher ratings than female candidates and younger candidates" | Reframed to: bias runs specifically against older women at the age/gender intersection | Original framing understated the finding; Stanford's paper identifies older women as the harmed group, not merely that men were favored |
| SAP Joule + Winston integration | "integrating with SAP's Joule AI" (implied near-term) | "connected as linked agents — combined integration available H2 2026" | SAP confirmed H2 2026 timeline; source: SAP News Center Mar 2026 |

### scoring-rubric.md

| Change | Old | New | Reason |
|---|---|---|---|
| ATS keyword match rate | "65–75% to pass modern AI-powered ATS screening" | "65–75% threshold; aim for 80%+ for competitive roles" | Research found practitioners increasingly advise 80%+ for high-volume or competitive postings; Jobscan's own guidance has shifted upward |

---

## 2026-03-25 — scoring-rubric: remove hardcoded weights, fix file format advice

**File:** `scoring-rubric.md`
**Trigger:** Weights moved from reference file to SKILL.md so they can vary by role archetype

| Change | Old | New | Reason |
|---|---|---|---|
| Section headers | Included hardcoded weights (e.g., "Technical Skills (30% weight)") | Weights removed from headers | Weights differ by role archetype (IC Technical, People Leadership, Cross-Functional); hardcoding one set was misleading |
| File format advice | "PDFs are increasingly supported by modern ATS, but `.docx` is still safer when unsure" | "Text-based PDF is now the recommended default; use .docx only for iCIMS, Taleo, or if explicitly requested" | Reflects 2025–2026 consensus; PDF default is now accurate for most platforms |
| Intro line | "Detailed criteria for scoring each of the five evaluation dimensions." | Added note pointing to SKILL.md for weight sets | Cross-reference added to avoid confusion |

---

## 2026-03-25 — ai-screening-research.md: major research refresh

**File:** `ai-screening-research.md`
**Trigger:** Initial content based on pre-2024 knowledge; refreshed against 2025–2026 primary sources

### Methodology and framing

| Area | Change | Reason |
|---|---|---|
| "75% rejected by ATS" stat | Explicitly debunked and removed | Traces to Preptel (closed 2013); no documented methodology; cited widely but fabricated |
| Adoption table | Replaced bullet list with sourced table including confidence notes | More scannable; citations visible |
| Tool landscape | Rewrote entirely | M&A activity in 2024–2025 changed the market significantly |
| "Modern AI: semantic embeddings" section | Replaced with three-layer model (Parsing / Scoring / AI Co-Pilot) | More accurate to how enterprise ATS actually work; co-pilot LLM layer was absent from original |
| Platform tiers | Added Legacy / NLP / Vector / No-AI / Conversational taxonomy | Clearer than generic "modern AI" grouping |

### Key factual additions

- Workday + HiredScore acquisition (March 2024) and A/B/C/D grading model documented
- HiredScore explicitly noted as non-generative AI (chose explainability; all decisions auditable)
- Eightfold RNN architecture documented (sequence modeling of career trajectory)
- Greenhouse confirmed as no native AI scoring — human-in-the-loop by design
- BambooHR added (no AI scoring; SMB HRIS)
- Paradox (Olivia) clarified as conversational top-of-funnel tool, not resume ranking
- Taleo documented as maintenance mode; Oracle Recruiting Cloud migration active
- Formatting failures section expanded with specific causes (Canva PDFs, scanned PDFs, text boxes, headers/footers)
- Keyword density sweet spot added: 15–25 keywords at 2–3% word count; stuffing detection noted
- Manipulation triggers section added: white-font, prompt injection, near-verbatim JD copy
- Short tenure and employment gap sections added with ATS mitigation strategies
- Career change paths documented for traditional ML vs. vector/embedding systems
- HireVue section: facial analysis confirmed discontinued Jan 2021; STAR scoring framework noted; 70M+ training interviews
- AI content detection section added with employer policy spectrum (TopResume 2025, Resume Now 2025)
- Bias section added: Brookings 2025 (racial/gender), Stanford Oct 2025 (age), UW Nov 2025 (bias amplification)
- Regulatory section added: EU AI Act timelines, NYC Local Law 144, Mobley v. Workday litigation
- Cover letter trends: 83% of hiring managers reading cover letters (Resume Genius 2025)
- Key Takeaways section added as quick-reference summary
- Sources section added with full citation list

---

## Format

Each entry documents:
- **Date** — when the change was made
- **File(s)** — which reference files were affected
- **Trigger** — what prompted the change (research pass, feedback, new study, etc.)
- **Change table** — what changed, old vs. new, and why

When a major claim is updated, the original source and the replacement source are both noted.
