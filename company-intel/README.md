# Company Intel Skill

Generic cover letters get ignored. The candidates who stand out walk in knowing what the company is actually focused on right now — not what their website says, but what they said in earnings calls, blog posts, and press releases last quarter. This skill does that research automatically and tells you exactly what to mention, what to avoid, and what they're likely to pay.

---

## What to Give It

You need either a company name or a job description — or both.

| Input | How to provide it |
|---|---|
| Company name | Just say it: `research Stripe` |
| Job description | Put the file in your folder, or paste the text |
| Both | Gives sharper results — role and team context improves research targeting |

If you give it a job description, it extracts the company name, role, and team context automatically before researching.

---

## What You Get Back

Results are saved to `intel-brief.md` in your working directory. If you run `resume-review` afterward, it picks up this file automatically — no need to re-run the research.

### Report sections explained

**Company Snapshot**
3–5 sentences on what the company does, their business model, scale, and recent trajectory. Specific enough to reference naturally in conversation.

**What This Company Cares About Right Now**
Their current priorities — not generic values, but specific things they're actively investing in or trying to fix, grounded in recent announcements, earnings calls, or hiring patterns. These are the things worth referencing in your cover letter.

**The Team / Product Context**
What's known about the specific team, product, or initiative the role sits within — stage, recent launches, known challenges, team size if available. Only included if role/team context was provided.

**Cover Letter Recommendations**
Specific things to mention in your cover letter, each tied to a concrete research finding. Includes example phrasing and the source behind each recommendation.

**Resume Tailoring Recommendations**
Keyword and framing adjustments to make your resume resonate with this company — which terms to add, which achievements to surface, how to shift emphasis.

**Salary Intelligence**
Compensation range for the role at this company, broken into low / median / high with sources and recency noted. Draws from Glassdoor, Levels.fyi, Blind, Reddit, and public H-1B visa / PERM (Program Electronic Review Management) labor certification filings where available.

**Employment Reviews Summary**
Patterns from recent employee reviews — recurring positives, recurring concerns, red flags (layoffs, reorgs, rating trajectory), and what the interview process typically looks like. Outliers are filtered out in favor of patterns.

**Political Disposition & Public Advocacy**
Where the company sits on the political spectrum based on public records only — Political Action Committee (PAC) / Federal Election Commission (FEC) donation history, federal lobbying disclosures, official policy positions (Diversity, Equity & Inclusion (DEI), Environmental, Social & Governance (ESG)), CEO public statements, and industry association memberships. Presented as factual signals without editorial framing. Useful for culture-fit assessment.

**Things to Avoid**
Topics or framings that could land awkwardly — recent layoffs you shouldn't cite as a positive signal, product lines that were discontinued, competitive tensions with your current employer.

**Research Confidence**
Honest assessment of how much public information was available in each category. Private companies and stealth startups often have thin coverage — the brief will say so rather than filling gaps with guesses.

---

## Reference Files

### `references/research-sources.md`
The methodology behind where and how the skill searches. Useful if you want to understand why certain sources are trusted more than others, or if you're researching a company type that's less common.

- **Source reliability ranking** — four tiers from most to least reliable, with reasoning. Company engineering blogs and earnings call transcripts (Tier 1) carry more weight than Glassdoor reviews (Tier 3) or Wikipedia (Tier 4).
- **Salary research by company type** — different playbooks for big tech, startups, nonprofits, and government contractors. Includes how to interpret base vs. total comp, recency, and geographic adjustments.
- **Employment review calibration** — what patterns to look for vs. ignore (Glassdoor skews toward dissatisfied employees; Blind skews toward engineers). How to weight review trends vs. absolute scores.
- **Search patterns by company type** — specific search templates for public companies, growth-stage startups, early-stage/stealth, enterprise, nonprofits, and government contractors.
- **JD signals to research further** — a table of phrases that appear in job descriptions (e.g., "we're rebuilding X", "fast-growing", "cross-functional") and what each one means you should look up.
- **When research turns up little** — how to handle thin-coverage companies (stealth startups, private companies with no public presence) without padding the brief with guesses.

---

## Tips

- **Run this before resume-review** — the intel brief is automatically reused by `resume-review` if it's in the same folder, skipping the research step and saving significant time
- **Specificity beats volume** — the brief prioritizes recent, concrete findings over generic company descriptions. If research turns up little, it says so rather than padding with filler
- **Salary data varies by source** — H-1B/PERM filings (available for public companies and government contractors) are the most reliable because they're legally required disclosures. Glassdoor and Blind reflect self-reported data
- **Political disposition is factual, not advisory** — the skill reports what public records show and doesn't suggest whether that's good or bad. You decide what matters to you
- **The brief goes stale** — research is timestamped; if you're re-running `resume-review` more than 30 days later, delete `intel-brief.md` to force a fresh research pass
