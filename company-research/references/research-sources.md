# Research Sources & Search Patterns

## Source Reliability Ranking

| Tier | Source Type | Why It's Valuable |
|---|---|---|
| 1 | Company's own blog (engineering, product, company) | Authentic voice, specific initiatives, often reveals actual priorities |
| 1 | Earnings calls / investor day transcripts | Executives say what they actually care about growing or fixing |
| 1 | Recent press releases (last 6–12 months) | Specific launches, partnerships, strategic moves |
| 1 | H1B/PERM public filings | Actual salary figures filed with the government; highly reliable for companies that sponsor visas |
| 2 | Company careers page / life page | Values language, team culture framing, what they emphasize to recruits |
| 2 | LinkedIn company page (recent posts) | What they're publicly proud of, recent milestones, culture signals |
| 2 | Tech/trade press coverage (TechCrunch, Wired, industry outlets) | External validation, customer/market context |
| 2 | levels.fyi | Crowdsourced but well-validated compensation data, especially strong for big tech |
| 3 | Glassdoor salary estimates | Directionally useful; self-reported, verify with other sources |
| 3 | Glassdoor / Blind (reviews) | Useful for tone calibration and pattern detection, not for facts |
| 3 | Job postings for adjacent roles | Reveals team priorities and what skills they're investing in |
| 4 | Wikipedia / Crunchbase | Background only; often stale |

**Avoid:**
- Content marketing pieces with no substance
- Recycled press coverage that all sources from the same original release
- Review sites for factual claims about the company
- Single outlier reviews (1-star or 5-star) without corroboration from a pattern

---

## Salary Research Sources

### Best sources by company type

**Big tech / public companies:**
- levels.fyi — most reliable crowdsourced TC data for FAANG+ and large tech; shows base/bonus/equity breakdown
- H1B salary disclosure search: `site:h1bdata.info "[Company]" "[role title]"` or `flcdatacenter.com`
- Glassdoor salary for cross-check

**Startups / private companies:**
- Glassdoor salary (limited data, use as floor estimate)
- Blind threads: search `"[Company]" "[role title]" TC OR compensation site:reddit.com/r/cscareerquestions OR site:teamblind.com`
- Levels.fyi if they're large enough to appear
- Job posting itself — some states (CA, NY, CO, WA) legally require salary ranges in postings

**Non-tech / traditional industries:**
- Glassdoor and Indeed salary estimates
- Bureau of Labor Statistics OES data for the occupation code
- Industry association salary surveys if available

### Interpreting salary data

- **Base vs. total comp:** For tech roles, always distinguish. Equity can be 30–60% of TC at senior levels.
- **Recency:** Data older than 18 months is less reliable in volatile markets; flag it.
- **Level calibration:** A "Senior Engineer" at one company is not the same level as another. Try to find data for the specific level or band if possible.
- **Geographic adjustment:** Remote vs. SF vs. NYC vs. Austin have meaningfully different ranges even at the same company.
- **Data sparsity:** If fewer than 5 data points are available, say so and widen the range accordingly.

---

## Employment Review Research

### What to look for

**Positive signals:**
- Consistent themes around learning, autonomy, team quality, work-life balance
- High ratings (4.0+) sustained over 12+ months
- Positive sentiment from engineers/ICs specifically (not just management)

**Negative signals to flag:**
- Glassdoor rating declining over the last 6–12 months (trend matters more than absolute score)
- Multiple reviews mentioning the same concern independently (reorg, poor management, slow growth, bait-and-switch on role)
- "CEO approval" rating below 60% — signals internal trust issues
- Recent layoffs (search `"[Company]" layoffs site:layoffs.fyi` or `techcrunch.com`)
- Glassdoor reviews mentioning "recent changes" or "used to be better" — signals cultural shift

**Interview process:**
- Glassdoor interview reviews often describe format, difficulty, and what's tested
- Search: `"[Company]" interview process "[role title]" site:glassdoor.com OR site:reddit.com`
- Useful for candidate prep, not just research

### Calibration notes

- Glassdoor skews toward dissatisfied employees (people who leave are more likely to review)
- Blind skews toward engineers at tech companies and can be harsh
- Balance both with the company's own messaging and tenure data
- Look for the ratio of positive to negative reviews, not just the existence of complaints

---

## Search Patterns by Company Type

### Public Companies

```
"[Company]" earnings call highlights 2025
"[Company]" investor day priorities
"[Company]" CEO interview strategy
"[Company]" 10-K OR annual report key initiatives
site:ir.[company].com
```

Focus: what leadership is measured on, what they've publicly committed to, what's growing vs. what's being cut.

### Growth-Stage Startups (Series B–D)

```
"[Company]" TechCrunch OR VentureBeat announcement
"[Company]" funding round 2024 OR 2025 OR 2026
"[Company]" engineering blog
"[Company]" product launch OR feature announcement
```

Focus: what problem they're solving, who their customers are, what stage of growth they're in (product-market fit vs. scaling vs. enterprise push). Their blog is often the richest source.

### Early-Stage / Stealth

```
"[Company]" site:linkedin.com
"[Company]" founder interview
"[Company]" YC OR "Y Combinator" OR "a16z" OR investor name
```

Expectation-set: limited public info is normal. Focus on what the JD itself reveals and any founder/investor public statements. Flag low research confidence clearly.

### Enterprise / Large Corp

```
"[Company]" "[division or product from JD]" announcement
"[Company]" digital transformation OR modernization initiative
"[Company]" "[role title]" team blog OR engineering
site:[company].com blog OR engineering OR newsroom
```

Focus: the specific division matters more than the parent company. A role in AWS is very different from a role in Amazon Retail. Dig into division-level intel where possible.

### Nonprofit / Mission-Driven

```
"[Org]" annual report 2024 OR 2025
"[Org]" strategic plan OR impact report
"[Org]" program OR initiative launch
```

Focus: mission alignment is critical here. Candidates should be able to speak specifically to the organization's programs and impact, not just the cause area.

### Government Contractors / Defense

```
"[Company]" contract award site:defense.gov OR site:usaspending.gov
"[Company]" program OR capability announcement
"[Company]" clearance OR CMMC OR FedRAMP
```

Focus: what contracts they hold, what agencies they serve, relevant compliance posture (FedRAMP, CMMC, etc.).

---

## JD Signals to Research Further

When these appear in a JD, do additional targeted research:

| JD Signal | What to Research |
|---|---|
| Named product or platform | Find product page, launch announcements, engineering blog posts about it |
| "We're rebuilding X" or "modernizing Y" | Look for blog posts, talks, or engineering posts about the migration/project |
| Specific methodology (e.g., "shape up", "OKRs", "DDD") | Confirms culture; look for how the company talks publicly about their process |
| Named competitor | Understand the competitive positioning the candidate is stepping into |
| "Fast-growing" or "scaling rapidly" | Find headcount growth data, recent funding, expansion announcements |
| "Cross-functional" or "working with executives" | Look for org signals about how empowered this team is, who they report to |
| Specific geography or market expansion | Find any expansion announcements, international launch news |

---

## When Research Turns Up Little

Some companies have minimal public footprint. Handle gracefully:

1. **Note the gap honestly** in the Research Confidence table
2. **Extract more from the JD itself** — the language, tone, and emphasis in a JD are primary sources. What do they repeat? What do they emphasize? What's the vocabulary?
3. **Use LinkedIn job posting patterns** — search for other open roles at the company to triangulate team priorities
4. **Suggest the candidate do primary research** — LinkedIn connections, informational interviews, reaching out to current employees before applying
