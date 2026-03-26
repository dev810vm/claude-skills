---
name: company-research
description: This skill should be used when the user wants to "research a company for a job application", "find out what to mention in my cover letter", "what should I say about the company in my resume", "tailor my application to this company", "what does this company care about", "research before applying", "what should I know about this company before applying", or provides a job description and wants company-specific talking points for their cover letter or resume. Use this skill whenever the goal is to surface company intelligence that makes an application more targeted and specific.
version: 1.0.0
---

# Company Research for Job Applications

Research a company using the job description as a starting point, then produce targeted recommendations for what to mention in a cover letter and resume to make the application feel specific, informed, and well-matched.

## Inputs

The user provides either:
- A **job description** as a file (PDF, TXT, DOCX) or pasted text, OR
- A **company name** (and optionally a role title or website URL)

Either input is sufficient to run the full research process.

**If a job description is provided, extract before researching:**
- Company name
- Role title and team/department if mentioned
- Any product names, initiatives, or priorities mentioned
- Any cultural language or values signals in the JD text itself

**If only a company name is provided:**
- Use it directly as the research target
- Role title and team context will be unknown — note this in the output and proceed with company-level research
- If the user also supplied a role title or URL, use those to sharpen the research

**If neither a company name nor a job description is provided, ask:**
> "What company should I research? You can share a company name, a job description (as a file or pasted text), or both."

---

## Research Process

### Step 1: Identify Research Targets

From the JD (if available) or the user-provided company name, determine:
- Company name and primary website domain
- Whether this is a known public company, startup, nonprofit, or subsidiary
- Any specific product lines, divisions, or teams referenced (from JD or user context)

### Step 2: Run Web Research

**Use the Agent tool to run all web research in parallel.** Pass the company name, role title (if known), and the 8 research categories below. Instruct the agent to fire ALL WebSearch and WebFetch calls simultaneously — do not wait for one to complete before starting the next. The agent should return results organized by category.

> Agent prompt template: "Run all of the following web searches and fetches simultaneously. Return results organized by category. Company: [name]. Role: [title or 'unknown']. [paste all searches below]"

All 8 categories should launch at the same time. Within each category, all searches also fire simultaneously.

---

**Category 1 — Company fundamentals** (run all simultaneously):
- Search: `"[Company name]" mission values culture`
- Search: `"[Company name]" recent news 2025 2026`
- Fetch the company's About page
- Fetch the company's Careers/Culture page if accessible

**Category 2 — Business context** (run all simultaneously):
- Search: `"[Company name]" strategy growth product roadmap`
- Search: `"[Company name]" funding revenue customers OR "[Company name]" annual report`
- For public companies: Search recent earnings call highlights or investor day summaries

**Category 3 — The specific team/product** (run all simultaneously):
- Search: `"[Company name]" "[team or product from JD]" engineering blog OR product update`
- Search: `"[Company name]" "[role title]" team priorities OR challenges`

**Category 4 — Culture and values signals** (run all simultaneously):
- Fetch the company's careers page or "life at [company]" page
- Search: `"[Company name]" glassdoor culture OR employee reviews` (for tone signals, not for complaints)
- Search: `"[Company name]" engineering blog OR product blog`

**Category 5 — Recent developments (last 12 months)** (run all simultaneously):
- Search: `"[Company name]" announcement launch partnership 2025 OR 2026`
- Search: `"[Company name]" press release site:businesswire.com OR site:prnewswire.com`

**Category 6 — Salary data** (run all simultaneously):
- Search: `"[Company name]" "[role title]" salary site:glassdoor.com`
- Search: `"[Company name]" "[role title]" salary site:levels.fyi` (especially for tech roles)
- Search: `"[Company name]" "[role title]" compensation site:blind.com OR site:reddit.com`
- Search: `[role title] salary "[Company name]" 2025 OR 2026`
- For public companies or government contractors: Search `"[Company name]" H1B salary disclosure OR PERM filing "[role title]"` — public records with actual comp figures
- Collect a range: low, median, high, and note the source and recency of each data point

**Category 7 — Employment reviews** (run all simultaneously):
- Search: `"[Company name]" glassdoor reviews 2024 OR 2025 OR 2026`
- Search: `"[Company name]" layoffs OR "hiring freeze" OR "reorg" 2024 OR 2025 OR 2026`
- Search: `"[Company name]" work life balance OR "interview process" site:glassdoor.com OR site:blind.com`
- Look for patterns across multiple reviews rather than outliers; note review recency
- Flag any significant recent negative signals (mass layoffs, exec turnover, culture shifts)

**Category 8 — Political disposition and public advocacy** (run all simultaneously):
- Search: `"[Company name]" political donations OR PAC site:opensecrets.org`
- Search: `"[Company name]" lobbying disclosure OR federal lobbying`
- Search: `"[Company name]" CEO political statement OR endorsement OR public position`
- Search: `"[Company name]" DEI OR diversity equity inclusion policy 2024 OR 2025 OR 2026`
- Search: `"[Company name]" ESG OR sustainability OR environmental policy`
- Search: `"[Company name]" social policy stance OR immigration OR LGBTQ OR abortion` — only report if official company statements exist; do not report speculation or individual employee views
- Note industry association memberships that carry a known political lean (e.g., Business Roundtable, Chamber of Commerce, or progressive equivalents)
- Only document **official company-level signals**: FEC/OpenSecrets records, lobbying disclosures, formal policy statements, CEO official communications
- Do **not** infer from employee reviews, individual donations, or social media speculation
- Present signals descriptively — state what the evidence shows, not whether it is good or bad

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

### Political Disposition & Public Advocacy

**Disposition signal:** [Conservative-leaning / Progressive-leaning / Mixed / No public signals found]

*Based on: [one-line summary of evidence basis — e.g., "PAC donation history and CEO public statements"]*

**Evidence:**

| Signal type | Finding | Source |
|---|---|---|
| Political donations (PAC/FEC) | [What was found, or "No data found"] | [opensecrets.org / fec.gov] |
| Federal lobbying | [Issues lobbied on, or "None on record"] | [source] |
| Official policy positions | [e.g., DEI commitments, ESG pledges, public stances] | [source] |
| Leadership public statements | [Any CEO/exec public political statements, or "None found"] | [source] |
| Industry associations | [Memberships with political alignment signals, or "None identified"] | [source] |

**Gaps / caveats:**
- [Note if data was sparse, conflicting, or limited to one signal type]
- [Note if the company is private and has less required public disclosure]

> All findings reflect publicly available records and official statements only. Individual employee views and speculation are excluded. Political disposition does not predict individual team or manager culture.

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
| Political disposition | High / Medium / Low | [why] |

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
- **Political disposition is descriptive, not prescriptive.** Report what the evidence shows — PAC filings, lobbying records, official statements. Never characterize a company's political position as a positive or negative signal. The candidate determines what matters to them.

## Additional Resources

- **`references/research-sources.md`** — Source types ranked by reliability, and search patterns for different company types (startup, enterprise, nonprofit, government contractor)
