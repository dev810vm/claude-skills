# AI Screening in Hiring — Research Reference (2025-2026)

Use this when evaluating how a resume will perform against AI screening systems, and when giving application strategy advice.

---

## Scale and Adoption

- 83% of companies use AI for resume screening (2025)
- 98% of Fortune 500 companies use ATS
- 75% of resumes are filtered before a human sees them
- 21% of companies auto-reject candidates at all stages without human review
- 92% of ATS rank candidates rather than hard-reject on content — but being ranked low has the same practical effect

Company size correlation:
- Fortune 500: near-universal AI screening
- Mid-size (250–1,000): ~75% use automated screening
- Small (<250): ~37%

---

## The Tool Landscape

### Legacy (rule-based keyword matching)
**Taleo** (Oracle), **SAP SuccessFactors**, older **iCIMS** and **Greenhouse** configs. Unforgiving of formatting issues and synonym mismatches. Still widely deployed.

### Modern AI-powered platforms

**Workday + HiredScore** (acquired April 2024): Enterprise-scale AI scoring using 11+ years of training data. Generates explainable candidate scores. Center of major employment discrimination litigation (*Mobley v. Workday* — conditionally certified class action under ADEA, covering ~1.1 billion application rejections).

**Eightfold AI**: Uses deep learning trained on 1.5B+ career profiles. Matches on skills, potential, and career trajectory — not just current titles. Can infer what a candidate could learn. Especially used for non-traditional background candidates.

**iCIMS**: Role Fit scoring via AI-powered ranking. More cautious on automation, invests in bias audits.

**Lever**: AI Talent Intelligence via NLP skill extraction and candidate ranking. Integrates with third-party AI tools.

**Greenhouse**: Deliberately no automated AI candidate scoring. AI used for admin tasks only (interview questions, JD generation). All evaluation decisions are human-in-the-loop. Candidates applying through Greenhouse reach a human reviewer.

**Paradox (Olivia)**: Conversational chatbot that handles top-of-funnel via SMS/chat. Common in high-volume hourly hiring. Runs knockout questions conversationally — a "No" on any hard threshold is instant disqualification. Does not evaluate competencies.

**SeekOut**: Sourcing tool only — recruiters use it to find candidates who haven't applied. Not relevant for inbound applications.

**HireVue**: Dominant AI video interview platform. See dedicated section below.

---

## How Modern AI Scores Resumes

### Legacy: exact keyword matching
Literal string matching. "Software Engineer" ≠ "Software Developer." Tables, graphics, and columns cause parsers to drop content. Fails by being too rigid.

### Modern AI: semantic embeddings
Transformer-based models (BERT, RoBERTa, GPT-family) convert JDs and resumes into high-dimensional vectors. Cosine similarity between vectors produces a relevance score. This approach:
- Recognizes synonym relationships
- Evaluates full context, not just keyword presence
- Learns from recruiter feedback loops over time
- Still anchors on the JD's language — mirroring that language improves scores

**ATS score benchmarks:**
- Below 60%: almost always filtered
- 70–80%: threshold for most Fortune 500
- 80%+: competitive for most roles
- 85%+: target for high-competition roles

---

## Signals AI Evaluates Beyond Keywords

**Tenure patterns**: Short tenures (<18 months across consecutive roles) trigger negative signals in systems trained on historical data. Contract/agency work is an exception — label it clearly.

**Career trajectory coherence**: Eightfold and similar tools model whether your progression is consistent with how successful people move through similar careers. Gaps and lateral moves can score poorly if unexplained.

**Skills density**: Skills *demonstrated in bullets* score higher than skills *only listed*. Modern AI weights evidence over assertion.

**Quantification**: Bullets with specific numbers (%, $, headcount, time) receive higher relevance scores. Research-backed target: 60–70% of experience bullets should include a measurable result.

**Skills section placement**: 60%+ of AI systems filter on skills before reading job history. Skills buried at the bottom may not influence the first-pass filter.

**Summary section weight**: AI scores the summary heavily because it appears first and sets the semantic context for the rest of the document.

**Prestige and institutional bias**: AI trained on past successful hires can learn to weight credentials from brand-name universities or employers — a documented failure mode, not an intentional feature.

**Employment gaps**: Unexplained gaps are penalized in training-data models. Any honest framing (consulting, caregiving, retraining) scores better than silence.

**Application timing**: Early applicants often surface first in recruiter views. Apply within 48–72 hours of a posting going live.

---

## HireVue: AI Video Interviews

**What it evaluates now (post-2021):**
- Transcribed content — what you say, structure, vocabulary, evidence of competencies
- Speech patterns (pace, filler words) — appear verbatim in transcript
- Answer structure (STAR format scores well)
- Response relevance to the question

**What it no longer claims to evaluate:**
- Facial expressions (discontinued 2021 under regulatory pressure)
- Physical cues and eye contact

**Scoring baseline**: Candidates are compared to top performers at that company in similar roles — not a generic benchmark.

**Training data**: 70M+ interviews.

**Transparency problem**: CDT review found HireVue's explainability statement does not adequately disclose which signals drive scores or their weights.

**Candidate guidance:**
- STAR format for every behavioral question
- Front-load Action and Result — don't build up to the answer
- 90–120 seconds per answer
- Minimize filler words (appear in transcript)
- Neutral background, eye-level camera, well-lit, quiet
- Game-based assessments (cognitive/personality): cannot be gamed; approach calmly

---

## Specific Causes of AI Filtering

**Formatting failures:**
- Tables, text boxes, multi-column layouts scramble parsing
- Graphics, icons, photos are invisible to parsers
- Headers/footers often stripped — don't put key info there only
- Canva templates generate PDFs that break ATS parsing
- DOCX is safer than PDF for most systems

**Content gaps:**
- Using synonyms instead of JD's exact terminology in key skills areas
- Missing explicit mention of required credentials set as knockout criteria
- No skills section, or skills section buried below experience

**Knockout question failures:**
- A single "No" answer to a hard-threshold question = instant disqualification
- Binary — not scored, not graduated

**Manipulation triggers:**
- White font/hidden text — detected by parsers, visible when downloaded, results in blacklisting
- Prompt injection ("Ignore previous instructions") — actively detected
- Near-verbatim JD copy — flagged as suspicious by semantic systems
- Keyword stuffing — modern AI detects and down-ranks

**Behavioral signals:**
- Multiple short tenures without context
- Unexplained employment gaps
- Applying to many roles at the same company in a short window (some ATS track this)

---

## AI-Written Content Detection

**Detection accuracy**: Poor for software tools (OpenAI shut down its classifier in 2023; GPTZero, Originality.ai produce significant false positives).

**Human detection**: 67% of hiring managers report identifying obvious AI content by pattern recognition — generic phrasing, uniform structure, lack of specific details, tone mismatch.

**Employer policy spectrum:**
- 30.3% draw a hard line at AI for resume writing
- 25% say cover letters must be entirely human-written
- Most are ambivalent if content is personalized and accurate
- 62% report rejecting AI-generated resumes that lack personalization

**The practical risk**: AI-generated content that passes screening but fails in interviews — the candidate can't speak naturally to what they wrote.

**Safe approach**: Use AI to draft, then heavily edit with specific examples, concrete numbers, and authentic voice. If you can't explain it in an interview, don't include it.

---

## Cover Letter Trends

83% of hiring managers now report reading cover letters — up sharply. As AI homogenizes resumes, specific and authentic cover letters are differentiators. Coaching consensus:
- Open with a concrete hook (real number, specific project, genuine reason for this role)
- Mirror 2–3 key terms from the JD
- Include one concrete recent outcome
- Keep to half a page or less
- Explain what you offer, not what you want

---

## Documented Bias in AI Hiring Systems

**Racial bias (Brookings, 2024):**
- White-associated names preferred in 85.1% of comparisons vs. Black-associated names in 8.6%
- Equal selection in only 6.3% of tests across 40,000 resume-JD comparisons

**Gender bias:**
- Men's names favored 51.9% vs. women's 11.1% of the time

**Age bias (Stanford, 2025):**
- Older male candidates received higher ratings than female candidates and younger candidates in some tools — the opposite direction of common assumptions

**Mechanism**: AI trained on historical hiring data inherits historical biases as features. This is structural, not intentional.

**Regulatory context:**
- NYC Local Law 144 (effective July 2023): Requires annual bias audits and candidate disclosure for automated hiring tools
- Illinois, Colorado, California: Require bias mitigation measures
- EEOC has issued guidance on AI and employment discrimination

**Active litigation**: *Mobley v. Workday* — class action alleging racial, age, and disability discrimination via automated screening; ~1.1B application rejections in scope; class conditionally certified under ADEA as of 2025.

---

## Key Takeaways for Resume Review

1. File format: DOCX preferred over PDF for most ATS
2. Skills section: move above work experience; ensure skills appear with evidence in bullets
3. Quantification: target 60–70% of bullets with measurable results
4. Tailor every application: mirror JD language, target 80–90% keyword overlap
5. Apply early: first 48–72 hours after posting goes live
6. Employment gaps: any honest framing beats silence
7. Short tenures: provide context (contract, layoff, growth)
8. Knockout questions: answer carefully — one "No" is disqualifying
9. Cover letter: specific hooks, half page, explain what you offer
10. AI content: draft with AI, rewrite with specific authentic voice
11. LinkedIn: sync with resume before submitting
12. Never: white font, hidden text, prompt injection — detected and blacklisting risk
13. Tools: Jobscan, Rezi, or similar to verify keyword match before submitting

---

## Sources
- Brookings: Gender, Race, and Intersectional Bias in AI Resume Screening (2024)
- NPR: AI Hiring Tools — Bias and Bugs (Oct 2025)
- CDT: HireVue AI Explainability Statement Analysis
- Resume2Vec: Semantic Embedding Research (MDPI, 2025)
- Workday/HiredScore litigation coverage (CNN, FairNow, Norton Rose Fulbright, 2025)
- Hirelytica: ATS AI Platform Comparison (2025)
- The Interview Guys: AI Screening Adoption Statistics
- Cover Letter Copilot: Survey of 850+ Recruiters on AI Detection
- PassTheScan: ATS Technology Report (2025)
- ORISE: Resume Formatting for AI Screening
