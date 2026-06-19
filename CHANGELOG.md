# Changelog

All changes to this repo. Most recent first.

---

## 2026-06-19 (update 3)

### resume-review/SKILL.md — Step 10 video interview section updated

Four changes driven by new research in ai-screening-research.md:
- **Factual correction:** "Technical setup not scored by AI" → "these are active AI scoring variables" (arxiv 2505.12114: environmental factors shift AI personality scores more than candidate performance differences)
- **Interview Insights scope:** Added note that HireVue now AI-scores live/structured interviews via Interview Insights (Oct 2025) — not just async pre-recorded video
- **Voice AI interviewer:** Added note on Hireguide acquisition (Mar 2026) — candidates may encounter a real-time AI voice screening call; STAR structure still applies
- **Candidate rights:** Added explicit guidance on Illinois statutory right to decline AI video analysis and receive alternative evaluation (Illinois AI Video Interview Act 2026 amendment); noted parallel rights under NYC LL144 and Colorado SB205

---

## 2026-06-19 (update 2)

### ai-screening-research.md — major research sweep, 8 new findings

**Regulatory updates:**
- **Colorado SB205:** Corrected from "effective February 2026" → "enforcement currently paused" — federal court stay issued April 27, 2026; enforcement suspended while lawmakers reconsider timing and scope
- **Illinois AI Video Interview Act (amended February 2026):** Replaced brief mention with full dedicated section. Key change: explicit written consent now required before AI video interview (continuing ≠ consent). Added: right to alternative evaluation pathway if candidate declines, 30-day deletion requirement for recordings
- **California:** Added note on legislative watch status; CO SB205 is expected template

**Active litigation — two new cases:**
- **Mobley v. Workday 2026 updates:** Added March 6 ADEA certification, February 17 opt-in notice, and critical May 29, 2026 discovery rulings (bias-testing data shielded by attorney-client privilege; customer data not obtainable from Workday; EEO-1/OFCCP docs ordered produced). Added the privilege-shielding implication as a blueprint other vendors will follow.
- **Eightfold AI FCRA class action (January 21, 2026):** New full section. Theory: AI hiring assessments = consumer reports under FCRA, triggering disclosure and dispute rights. Filed by Outten & Golden + Towards Justice. Introduces "liability squeeze" concept — two independent legal theories (FCRA + employment discrimination) simultaneously pressuring AI hiring vendors.

**Documented bias — four new findings:**
- **Stanford/Northeastern/Chapman algorithmic monoculture (May 2026, ACM FAccT):** 4M+ applications, 156 employers ($5B+ revenue), all using Pymetrics/Harver. 26% of Black applicants and 15% of Asian applicants sent to adversely impacted positions. Systemic 10% rejection rate for multi-applicant candidates. 330-day score reuse means one algorithmic rejection propagates to all other Pymetrics employers in the window. Vendor concentration amplifies and replicates bias sector-wide.
- **ACLU complaint: Intuit + HireVue (March 2025):** Native American, deaf Intuit employee required to use HireVue for internal promotion; ADA captioning accommodation denied; subtitles absent during interview. Also alleges worse performance for non-White candidates speaking Native American English dialects. Claims: Title VII, ADA, Colorado ADA. HireVue denies. Implication: transcript-based scoring can encode dialect bias even after audio/face scoring is disabled.
- **Video interview environmental factors (arxiv 2505.12114, May 2026):** Background, lighting, and ambient noise alter AI personality assessment scores by more than candidate performance differences. Added to HireVue candidate guidance as active scoring variables.
- **LLM resume screening validity (arxiv 2602.18550, February 2026):** Models don't reliably abstain when ranking equally-qualified candidates; select different demographic groups at different rates. Added to Sources.

**HireVue product evolution section added:**
- Interview Insights (October 2025): competency-tagging in live/recorded interviews, talk-time and question-consistency measurement
- Workday AI Agent Network (January 2026): HireVue scores now trigger Workday workflow agents
- Hireguide acquisition (March 2026, ~$25–45M): voice-based conversational AI interviewer; replaces recorded video screening with real-time AI dialogue for initial qualification

---

## 2026-06-19

### resume-review/SKILL.md — fix internal stat inconsistencies
Three figures in SKILL.md disagreed with their own reference files; aligned SKILL.md to the reference-file values:
- **ATS adoption:** "83% of companies use AI for resume screening" → "~76%" (the 83% was the cover-letter-reading stat from ai-screening-research.md cross-wired into the ATS claim; reference value is ~76%, HeroHunt 2025)
- **Short tenure threshold:** "<18 months" → "<12 months" (matches scoring-rubric.md and ai-screening-research.md)
- **Employment gap threshold:** ">3 months" → ">6 months" (matches scoring-rubric.md and the Harvard Business School finding cited in ai-screening-research.md)

### ai-screening-research.md — Warden AI report + article validation pass
- Added **Colorado SB205** (effective Feb 2026, broadest US scope — covers developers and deployers) to Regulatory section
- Added **AI vs. human fairness baseline** from Warden AI "State of AI Bias in TA 2025" (150+ audits, 1M+ samples): AI avg impact ratio 0.94 vs. human 0.67; up to 39% fairer for women, 45% fairer for racial minorities — framed with vendor self-interest and self-selection caveats
- Added **methodological caveat** for lab-based bias studies (name-substitution/forced-choice tests measure LLM behavior, not production ATS, which strip PII and score individually)
- Added **candidate notification gap**: only 15% of candidates told AI is used; rights under NYC LL144 / Colorado SB205 / EU AI Act frequently not disclosed
- Added **age/disability audit gap**: 95% of bias audits cover only sex and race; only 5% test age or disability despite Mobley
- Added **NYC LL144 compliance reality**: ~38% vendor compliance despite law in effect since Jan 2023
- Added "Last validated: 2026-06-19" header
- Sources: Warden AI "State of AI Bias in Talent Acquisition 2025"; intelligentcv.app ATS rejection article

---

## 2026-03-27

### ai-screening-research.md — whitepaper research pass, major new findings

New peer-reviewed research added:
- **AI self-preferencing** (Xu et al., AAAI/ACM August 2025): LLMs prefer resumes generated by the same model at 68–92% rates; candidates using the same LLM as the screener are 23–60% more likely to be shortlisted. Unknowable without knowing what model the employer uses — reinforces heavy rewriting over light AI polish
- **Position bias** (MIT Computational Law Report 2025): LLMs screening resume batches select the first resume 87–100% of the time when candidates are equally qualified — new technical basis for apply-early guidance
- **Cultural/linguistic bias** (arxiv 2508.16673, August 2025): Formal academic English from non-Western traditions scores 0.4–0.5 points lower (1–5 scale) vs. direct American business English — operates through sentence structure and hedging patterns, not name/identity signals
- **Bias amplification quantified** (arxiv 2509.04404, September 2025): Humans align with AI hiring recommendations 75–90% of the time, even when they think they're overriding the AI. Low AI score primes human recruiter judgment
- **Eightfold validated outcomes** (Eightfold engineering blog, 688K employees): Match Score ≥ 4.0 → ~50% more promotions, 5pp higher retention. Confirmed as genuine performance predictor
- **Eightfold fairness benchmarking**: All general LLMs (GPT-4o, Claude, Gemini, DeepSeek) failed EEOC four-fifths rule; Eightfold purpose-built model passed
- **HireVue clarification**: Speech patterns (audio/tone/pace) also removed, not just facial expressions. Only transcript text scored. Transcription via Rev.ai with domain-adapted RoBERTa model
- **Oracle ORC default-off**: AI scoring requires manual enablement; Taleo migrations don't activate it automatically

### ai-screening-research.md — add Gem ATS
- Added Gem to tool landscape under new "Generative AI (criteria-matching)" tier
- Gem uses Azure OpenAI (generative AI), not legacy ML — architecturally different from Workday/Eightfold
- Documented scoring pipeline: PII stripping → criteria-level scoring → match explanation with citations
- Flagged that full application history (prior rejections, interview notes) travels with candidates
- Flagged NYC Local Law 144 compliance gap in Gem's public documentation
- Added Key Takeaway #17 for Gem / tech company applications
- Sources: gem.com product docs, gem.com blog, help.gem.com compliance FAQs, G2 2025, Contrary Research

---

## 2026-03-26

### resume-review — execution order fix
- **Problem:** background agent for company research completed after the report was already written, leaving company-intel-dependent sections empty
- **Fix:** Steps 3 (ATS) and 9 (Writing Quality) now run first in parallel (text-only, no web calls), then company research runs as a blocking synchronous Agent call, then Steps 2/4/5/6 proceed with full intel
- **Files:** `resume-review/SKILL.md`

### reference files — deep research validation pass
- Validated 47 claims in `ai-screening-research.md` against current sources; 31 confirmed, 4 corrected:
  - Workday + Paradox acquisition: closed Oct 1, 2025 (was "pending")
  - HireVue optimal response: 60–90s delivery (was 90–120s)
  - Stanford age bias study: reframed as bias *against older women* specifically
  - SAP Joule + Winston integration: H2 2026 timeline clarified
- `scoring-rubric.md`: ATS keyword match rate updated — 80%+ recommended for competitive roles
- **Files:** `resume-review/references/ai-screening-research.md`, `resume-review/references/scoring-rubric.md`

---

## 2026-03-25

### resume-review — v3.1.0
- Parallel file reads at startup (all files in one batch)
- Company research launched via background Agent immediately after Step 1 parse
- Phase boundary markers added to each evaluation step
- ATS keyword table: replaced internal jargon with plain-language columns and emoji status indicators
- Confidence score table: `Band` column replaced with plain English `Meaning` descriptions
- Quick Kill List added to output (top 5 most impactful changes, shown early in report)
- **Files:** `resume-review/SKILL.md`

### resume-review — allowed-tools frontmatter
- Added `allowed-tools` frontmatter field to pre-approve tool calls (Read, Write, Glob, Grep, WebSearch, WebFetch, Agent)
- Fixed field name from `allowedTools` (camelCase) to `allowed-tools` (hyphenated — correct per Claude Code docs)
- **Files:** `resume-review/SKILL.md`

### resume-review — intel-brief write fix
- Background agent was blocked from writing files in sandboxed context
- Fix: agent returns complete intel brief as response text; main thread writes `intel-brief.md` verbatim
- Agent prompt updated to explicitly list all required sections and forbid truncation
- **Files:** `resume-review/SKILL.md`, `company-intel/SKILL.md`

### scoring-rubric — remove hardcoded weights, fix file format advice
- Removed hardcoded dimension weights from section headers (weights vary by role archetype; moved to SKILL.md)
- Updated file format recommendation: text-based PDF is now the default; .docx only for iCIMS, Taleo, or explicit requests
- **Files:** `resume-review/references/scoring-rubric.md`

### ai-screening-research.md — major research refresh
- Debunked "75% rejected by ATS" statistic (traces to Preptel, closed 2013, no methodology)
- Rewrote tool landscape section to reflect 2024–2025 M&A: Workday+HiredScore, SAP+SmartRecruiters
- Added three-layer ATS model: Parsing / Scoring / AI Co-Pilot
- Added platform tier taxonomy: Legacy / NLP / Vector / No-AI / Conversational
- Added keyword density guidance, manipulation trigger section, career trajectory signals
- Added HireVue post-2021 capabilities, AI content detection, bias research (Brookings, Stanford, UW)
- Added regulatory section: EU AI Act timelines, NYC Local Law 144, Mobley v. Workday
- Added sources section
- **Files:** `resume-review/references/ai-screening-research.md`

### company-research → company-intel rename
- Renamed skill directory and all internal references from `company-research` to `company-intel`
- **Files:** `company-intel/SKILL.md`, `company-intel/README.md`, `resume-review/SKILL.md`

### company-intel — major skill update
- Now accepts company name OR job description as input (previously required JD)
- Step 2 restructured into 8 explicit parallel research categories via Agent tool delegation
- Added Political Disposition & Public Advocacy research category and output section
- Output file logic: skip write when called from background agent; return text only
- **Files:** `company-intel/SKILL.md`

### docs — README files
- Added `README.md` at repo root, `resume-review/README.md`, `company-intel/README.md`
- Each README explains all report sections, reference file methodologies, and scoring approach
- Acronyms spelled out on first use (ATS, IC, HR, JD, PAC, FEC, DEI, ESG, EU AI Act, UW)
- **Files:** `README.md`, `resume-review/README.md`, `company-intel/README.md`

---

## Earlier (pre-2026-03-25)

### resume-review — auto-detect files
- Skill now globs current working directory for resume, JD, and cover letter before asking the user
- Reads all versions of each file type (e.g., multiple cover letter drafts)
- **Files:** `resume-review/SKILL.md`

### resume-review — versioned output
- Output files are versioned: `[resume]-review-[company]-v1.md`, `v2.md`, etc.
- Each run produces a new file; previous runs are never overwritten
- Run comparison section added to report
- **Files:** `resume-review/SKILL.md`

### Initial commit
- `resume-review` skill with scoring rubric, reframe strategies, and ATS research reference files
- `company-research` skill (later renamed `company-intel`)
