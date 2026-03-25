---
name: company-research
description: This skill should be used when the user wants to "research a company for a job application", "find out what to mention in my cover letter", "what should I say about the company in my resume", "tailor my application to this company", "what does this company care about", "research before applying", "what should I know about this company before applying", or provides a job description and wants company-specific talking points for their cover letter or resume. Use this skill whenever the goal is to surface company intelligence that makes an application more targeted and specific.
version: 1.0.0
---

# Company Research for Job Applications

Research a company using the job description as a starting point, then produce targeted recommendations for what to mention in a cover letter and resume to make the application feel specific, informed, and well-matched.

## Inputs

The user provides a job description as a file (PDF, TXT, DOCX) or pasted text.

**If no job description is provided, ask:**
> "Please share the job description — as a file path or pasted text. Do you also have a company name or website URL to start from?"

**Extract from the JD before researching:**
- Company name
- Role title and team/department if mentioned
- Any product names, initiatives, or priorities mentioned
- Any cultural language or values signals in the JD text itself

---

## Research Process

### Step 1: Identify Research Targets

From the JD, determine:
- Company name and primary website domain
- Whether this is a known public company, startup, nonprofit, or subsidiary
- Any specific product lines, divisions, or teams referenced in the JD

### Step 2: Run Web Research

Use WebSearch and WebFetch to gather intelligence across these categories. Run searches in parallel where possible.

**Company fundamentals:**
- Search: `"[Company name]" mission values culture`
- Search: `"[Company name]" recent news 2025 2026`
- Fetch the company's About page and Careers/Culture page if accessible

**Business context:**
- Search: `"[Company name]" strategy growth product roadmap`
- Search: `"[Company name]" funding revenue customers OR "[Company name]" annual report`
- For public companies: search recent earnings call highlights or investor day summaries

**The specific team/product:**
- Search: `"[Company name]" "[team or product from JD]" engineering blog OR product update`
- Search: `"[Company name]" "[role title]" team priorities OR challenges`

**Culture and values signals:**
- Fetch the company's careers page or "life at [company]" page
- Search: `"[Company name]" glassdoor culture OR employee reviews` (for tone signals, not for complaints)
- Look for any published engineering or product blog

**Recent developments (last 12 months):**
- Search: `"[Company name]" announcement launch partnership 2025 OR 2026`
- Search: `"[Company name]" press release site:businesswire.com OR site:prnewswire.com`

**Salary data:**
- Search: `"[Company name]" "[role title]" salary site:glassdoor.com`
- Search: `"[Company name]" "[role title]" salary site:levels.fyi` (especially for tech roles)
- Search: `"[Company name]" "[role title]" compensation site:blind.com OR site:reddit.com`
- Search: `[role title] salary "[Company name]" 2025 OR 2026`
- For public companies or government contractors: search `"[Company name]" H1B salary disclosure OR PERM filing "[role title]"` — these are public records with actual comp figures
- Collect a range: low, median, high, and note the source and recency of each data point

**Employment reviews:**
- Search: `"[Company name]" glassdoor reviews 2024 OR 2025 OR 2026`
- Search: `"[Company name]" layoffs OR "hiring freeze" OR "reorg" 2024 OR 2025 OR 2026`
- Search: `"[Company name]" work life balance OR "interview process" site:glassdoor.com OR site:blind.com`
- Look for patterns across multiple reviews rather than outliers; note review recency
- Flag any significant recent negative signals (mass layoffs, exec turnover, culture shifts)

### Step 3: Synthesize Findings

Organize findings into a structured intelligence brief. For each finding, note:
- What was found
- Why it's relevant to this specific role
- How a candidate could reference it authentically

Discard generic findings (e.g., "company values innovation") unless they're supported by specific, concrete evidence. Prioritize specific, recent, and role-relevant intelligence.

---

## Output Format

```
## Company Intelligence Brief

**Company:** [Name]
**Role:** [Title]
**Research date:** [today's date]

---

### Company Snapshot

[3–5 sentences: what the company does, business model, stage/scale, recent trajectory.
Specific enough that a candidate could drop this context naturally in conversation.]

---

### What This Company Cares About Right Now

[3–5 bullet points of specific, timely priorities — not generic values.
Each point should be grounded in a concrete source: a recent announcement, earnings comment, blog post, or hiring pattern.]

- **[Priority]**: [what's happening and why it matters to this role]
- ...

---

### The Team / Product Context

[What's known about the specific team, product, or initiative this role sits within.
Include: product stage, known challenges, recent launches, team size if known.]

---

### Cover Letter Recommendations

Specific things to mention, reference, or demonstrate in the cover letter — each tied to a concrete research finding.

1. **[Topic to mention]**
   - Why: [what the research shows the company cares about]
   - How to reference it: "[example phrasing or angle]"
   - Source: [where this came from]

2. **[Topic]**
   - Why: ...
   - How: ...
   - Source: ...

[3–6 recommendations, ranked by impact]

---

### Resume Tailoring Recommendations

Specific adjustments to make to the resume to resonate with this company — keywords to add, achievements to surface, framing to shift.

1. **[Recommendation]**
   - Why: [what the company signals it values]
   - Where to apply it: [summary, skills section, specific role bullets]
   - Example: "[before]" → "[suggested framing]"

[3–5 recommendations]

---

### Salary Intelligence

**Estimated compensation range for this role at this company:**

| | Amount | Source | Recency |
|---|---|---|---|
| Low end | $X | [source] | [year] |
| Median / Base | $X | [source] | [year] |
| High end / Total comp | $X | [source] | [year] |

**Notes:**
- [Any relevant comp structure signals: equity heavy? bonus-driven? flat bands?]
- [Geographic or level adjustments if applicable]
- [If data is sparse or conflicting, say so and note what's available]

---

### Employment Reviews Summary

**Overall sentiment:** [Positive / Mixed / Concerning] — based on [N] recent reviews

**Recurring positives:**
- [Theme, e.g., "strong engineering culture", "good work-life balance for a startup"]

**Recurring concerns:**
- [Theme, e.g., "slow promotion cycles", "unclear roadmap", "recent reorg created instability"]

**Recent red flags (if any):**
- [Layoffs, exec departures, Glassdoor rating trajectory, Blind sentiment shift]

**Interview process signals:**
- [Typical process length, format, what interviewers focus on, difficulty level]

> Note: review data reflects employee perceptions at a point in time and may not reflect current conditions. Weight recent reviews (last 12 months) more heavily than older ones.

---

### Things to Avoid or Be Careful About

[Optional — only include if research surfaces real signals]
- Any known sensitivities (recent layoffs, product pivots, competitive tensions) that could land awkwardly if referenced incorrectly
- Language or positioning that would sound out of sync with the company's actual culture

---

### Research Confidence

| Area | Confidence | Notes |
|---|---|---|
| Company fundamentals | High / Medium / Low | [why] |
| Team/product context | High / Medium / Low | [why] |
| Recent priorities | High / Medium / Low | [why] |
| Culture signals | High / Medium / Low | [why] |
| Salary data | High / Medium / Low | [why] |
| Employment reviews | High / Medium / Low | [why] |

[Note any significant gaps — e.g., "little public information about the [X] team specifically"]
```

---

## Output File

After producing the intelligence brief, write it to a markdown file in the same directory as the job description file (or the current working directory if the JD was pasted).

Write the complete brief to `intel-brief.md` in the same directory as the job description file (or the current working directory if the JD was pasted), then tell the user the full file path.

---

## Principles

- **Specific beats generic.** "They launched X in Q4 2025 and your infrastructure background maps directly to that initiative" is 10x more useful than "they value technical excellence."
- **Recency matters.** Prioritize findings from the last 12 months. Old information can embarrass a candidate who cites it as current.
- **Only recommend what can be referenced authentically.** Don't suggest a candidate fake familiarity with something. Frame recommendations as opportunities to demonstrate genuine alignment.
- **Flag gaps honestly.** If a company has minimal public presence and research turns up little, say so clearly — a candidate who over-researches a stealth startup looks out of touch.
- **Tie everything back to the role.** Company intel is only useful if it connects to the specific position. Filter out anything that doesn't have a clear application.

## Additional Resources

- **`references/research-sources.md`** — Source types ranked by reliability, and search patterns for different company types (startup, enterprise, nonprofit, government contractor)
