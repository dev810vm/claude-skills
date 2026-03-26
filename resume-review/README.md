# Resume Review Skill

Scores your resume against a job description, simulates how different screeners read it, flags gaps, and gives you a prioritized list of the most impactful changes to make.

---

## What to Give It

Put these files in the same folder and open Claude Code there:

| File | Required? | Notes |
|---|---|---|
| Your resume | Yes | PDF, DOCX, TXT, or any readable format |
| Job description | Recommended | PDF, DOCX, TXT, or paste the text |
| Cover letter | Optional | Analyzed separately if present |
| Additional materials | Optional | Writing samples, transcripts, Q&A responses |

Then say: `review my resume` — the skill finds the files automatically.

**No job description?** The skill runs in resume-only mode: formatting check, writing quality assessment, and bullet rewrites. Full scoring requires the job description.

---

## What You Get Back

The report is saved as `[resume-name]-review-[company]-v1.md` in the same folder. Every time you rerun it, a new versioned file is created (v2, v3, etc.) so you can track progress.

### Report sections explained

**Overall Match Score**
A percentage (0–100%) with a plain-English band:
- 85–100%: Strong Match — apply confidently
- 70–84%: Good Match — apply with targeted adjustments
- 55–69%: Moderate Match — address key gaps first
- 40–54%: Weak Match — significant gaps
- 0–39%: Poor Match — fundamental misalignment

**Dealbreakers**
Hard blockers that could disqualify you before anyone reads your resume — missing degree, required clearance, location conflict, hard experience floor. Check this first.

**Quick Kill List**
The top 5 highest-impact changes to make right now, ranked by how much they'll move your score. Start here if you're short on time.

**Company Intel Summary**
What the skill found out about the company and how it shaped the evaluation. Links to the full `intel-brief.md` for details.

**ATS Assessment**
How your resume performs against automated screening systems. Two scores:
- *Older systems (exact words only)* — legacy keyword matchers that need verbatim matches
- *Modern AI systems (includes synonyms)* — semantic systems that understand related terms

The keyword table shows every term from the job posting and whether it's in your resume:
- `✓ Found word-for-word` — safe on all systems
- `~ Implied — you used "[X]"` — safe for modern systems, but add the exact phrase to cover older ones
- `✗ Not found` — missing; add it if the experience exists

**Five-Persona Verdicts**
Your resume reviewed through five different lenses — ATS robot (0 seconds), recruiter glance (10 seconds), HR screen (30 seconds), hiring manager (2 minutes), technical reviewer (10 minutes). Each gives a binary verdict and the single factor that most drives their decision.

**Confidence-Scored Match Summary**
Every requirement from the job posting scored on how well your resume covers it:
- *Strong match* — you have it, cite it directly
- *Transferable* — you have a related version, bridge it explicitly
- *Partial match* — you've touched on it, mention it but don't lead with it
- *Weak* — thin evidence, address in cover letter
- *Not evidenced* — either truly missing or present but not documented; check which

**Gap Triage**
Gaps ranked by severity: Fatal (likely to disqualify) → Serious (weakens application) → Cosmetic (nice to fix but not decision-relevant). For each serious gap, the report either suggests a reframe strategy (if the experience exists but is poorly presented) or flags it as genuinely missing.

**Writing Quality**
Flags weak bullet patterns — duties instead of outcomes, AI-generated phrasing, vague action verbs, missing metrics. Includes rewrites of your 3 weakest bullets.

**Ceiling Analysis**
Your current score, your estimated score after the top 3 fixes, and your theoretical maximum given your background. If there's a hard ceiling (missing degree, missing years of experience), it tells you what would actually move it.

**Run Comparison** *(appears on v2+)*
Side-by-side score history across all versions so you can see what improved between runs.

---

## Scoring

Scores are weighted by role type, which the skill detects automatically:

| Dimension | Technical IC | People Leader | Cross-Functional |
|---|---|---|---|
| Technical Skills | 40% | 15% | 20% |
| Experience & Seniority | 25% | 35% | 25% |
| Domain Knowledge | 15% | 20% | 25% |
| Education & Credentials | 15% | 10% | 10% |
| Soft Skills & Culture Fit | 5% | 20% | 20% |

---

## Tips for Better Results

- **Fix the Quick Kill List items first** — these are ranked by score impact, not ease
- **If a keyword shows `~ Implied`**, add the exact JD phrase to your resume alongside your synonym — costs nothing and removes risk with older screening systems
- **"Not evidenced" ≠ "gap"** — if the skill flags something as not evidenced, check whether the experience is actually in your background but just not on your resume. Adding it could move the score significantly
- **Rerun after making changes** — each run produces a new versioned file so you can compare before/after
- **Add your cover letter** — it can resolve gaps the resume doesn't address, and the skill updates scoring accordingly
