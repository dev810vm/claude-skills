# Claude Code — Project Context

This repo contains Claude Code skills for job seekers. The mission is to help people beat AI hiring systems — automated resume screeners filter out qualified candidates at scale, and these skills fight back with better research, better resume targeting, and a clear view of how the machines score you.

---

## What Lives Here

```
resume-review/
  SKILL.md                        # The skill — invoked when user says "review my resume"
  README.md                       # Human-readable docs
  references/
    scoring-rubric.md             # Scoring criteria for the 5 evaluation dimensions
    reframe-strategies.md         # 4 strategies for turning weak matches into strong ones
    ai-screening-research.md      # How ATS and AI hiring systems actually work (2025-2026)

company-intel/
  SKILL.md                        # The skill — invoked when user says "research [company]"
  README.md                       # Human-readable docs
  references/
    research-sources.md           # Source reliability tiers, search patterns, salary methodology

CHANGELOG.md                      # All changes to this repo, most recent first
CONTRIBUTING.md                   # How to contribute updates
LICENSE                           # CC BY 4.0
```

---

## How Skills Work

Each skill is a `SKILL.md` file with YAML frontmatter and markdown instructions. Claude Code reads these files and follows the instructions when the skill is triggered.

**Frontmatter fields that matter:**
- `name` — the skill identifier
- `description` — trigger conditions; Claude Code uses this to decide when to invoke the skill
- `allowed-tools` — comma-separated list of tools pre-approved for this skill (Read, Write, Glob, Grep, WebSearch, WebFetch, Agent)

**Trigger:** Claude Code matches user intent against skill descriptions. If someone says "review my resume," the resume-review skill fires automatically.

---

## Development Workflow

When editing skills or reference files:

1. **Edit the file in this repo** (e.g., `resume-review/SKILL.md`)
2. **Copy to the global skills directory** so changes take effect immediately:
   ```bash
   cp -r resume-review ~/.claude/skills/
   cp -r company-intel ~/.claude/skills/
   ```
3. **Update CHANGELOG.md** with what changed and why
4. **Commit and push**

---

## Key Principles

**Don't break the neutrality of the Political Disposition section.** The company-intel skill researches political disposition from public records only — PAC filings, lobbying disclosures, official statements. It presents findings descriptively with zero editorial framing. Never add language that characterizes a company's political lean as good or bad.

**Don't encourage misrepresentation.** The reframe strategies in `references/reframe-strategies.md` are about making real experience visible and well-framed — not about fabricating skills or overclaiming. Any change that nudges candidates toward misrepresentation should be rejected.

**Specific beats generic.** The skills are only useful when output is concrete and tied to actual evidence. Generic advice ("tailor your resume", "highlight achievements") is worthless. Every recommendation should trace back to something specific.

**Reference files need to stay current.** The AI hiring landscape moves fast. `ai-screening-research.md` especially — ATS behavior, platform M&A, regulatory deadlines, and bias research all change. Target a re-validation pass every 6 months. When updating, document what changed and cite the source in CHANGELOG.md.

---

## Reference File Quick Summary

| File | What it does |
|---|---|
| `scoring-rubric.md` | Defines what 90%, 75%, 60%, etc. looks like for each scoring dimension. Also has ATS keyword priority tiers and formatting failure table. |
| `reframe-strategies.md` | Four strategies for 45–74% confidence matches: Keyword Alignment, Emphasis Shift, Abstraction Level, Scale Emphasis. Includes a decision tree for reframe vs. gap. |
| `ai-screening-research.md` | How real ATS platforms score resumes, formatting failures, career trajectory signals, HireVue guidance, bias research, regulatory landscape. Last validated 2026-03-26. |
| `research-sources.md` | Source reliability tiers, salary research by company type, employment review calibration, search patterns by company type (public, startup, enterprise, nonprofit, gov contractor). |
