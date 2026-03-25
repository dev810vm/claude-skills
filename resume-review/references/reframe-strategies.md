# Reframing Strategies for Weak & Adjacent Matches

Use these when a requirement has a confidence score of 45–74% (WEAK or ADJACENT). The goal is to make a genuine connection explicit without overclaiming.

A reframe is appropriate when the experience is real but the resume hasn't connected it to the requirement. It is NOT appropriate when the experience is absent — that's a gap, not a reframe opportunity.

---

## Strategy 1: Keyword Alignment

**What it does:** Preserve the exact meaning of an achievement but adjust the terminology to match the JD's vocabulary.

**When to use:** The candidate has the experience but uses different words. ATS and domain-insiders both need to see the expected terminology.

**Before:**
> "Built data pipelines to move clickstream events into our analytics warehouse"

**After:**
> "Engineered real-time ETL pipelines processing 50M+ daily clickstream events into Redshift for downstream ML feature engineering"

**Rules:**
- Don't add technologies you didn't use
- Don't elevate "contributed to" work to "owned" work
- Do use the exact tool names the JD uses when you used those tools

---

## Strategy 2: Emphasis Shift

**What it does:** Same facts, different framing — highlight the aspect of the work that maps to what this role values.

**When to use:** A role has multiple outcomes and the JD cares about one of them specifically. The current bullet emphasizes the wrong one.

**Before (for a business-outcome-focused role):**
> "Designed and implemented a distributed caching layer using Redis that reduced p99 latency by 40ms"

**After:**
> "Reduced checkout abandonment by 12% by cutting page load latency 40% through a Redis caching layer — translating directly to $2.1M ARR"

**Rules:**
- Both the technical and business framing must be true
- Don't fabricate impact numbers; use ranges or conservative estimates if exact figures aren't known
- The "shift" is in which fact leads, not in inventing new facts

---

## Strategy 3: Abstraction Level

**What it does:** Adjust how technically specific the language is — more abstract for business/leadership roles, more concrete for technical roles.

**When to use:** The role is at a different technical depth than the candidate's resume currently conveys.

**More abstract (for a VP or product role):**

Before: "Wrote Kubernetes operators in Go to automate cluster provisioning"

After: "Automated cloud infrastructure provisioning, reducing new environment spin-up from 3 days to 45 minutes and eliminating a class of deployment incidents"

**More concrete (for a senior IC role):**

Before: "Led backend development for the payments platform"

After: "Designed and owned the idempotency layer for payment processing in Go (gRPC + Postgres), handling 8K TPS with zero double-charge incidents over 18 months"

---

## Strategy 4: Scale Emphasis

**What it does:** Surface the cross-organizational scope, team size, budget, user base, or geographic reach that's implicit in the work but not stated.

**When to use:** The JD emphasizes scope, influence, or scale, and the resume describes work without indicating how big it was.

**Before:**
> "Led the migration from monolith to microservices architecture"

**After:**
> "Led 18-month monolith decomposition across 4 teams (22 engineers) serving 8M daily active users, with zero downtime during cutover"

---

## Decision Tree: Reframe vs. Flag vs. Gap

```
Is the experience genuinely present in the candidate's background?
├── No → GAP. Note it as missing. Don't reframe what isn't there.
└── Yes → Is it documented in the resume?
    ├── No → Instruct candidate to add it. It's invisible, not absent.
    └── Yes → Confidence score?
        ├── 75–100% → Already strong. Minor keyword alignment may help.
        ├── 60–74% → ADJACENT. Use Abstraction Level or Scale Emphasis.
        ├── 45–59% → WEAK. Use Emphasis Shift or Keyword Alignment.
        │             Flag for cover letter if reframe feels like a stretch.
        └── <45% → GAP. Acknowledge in cover letter or don't apply.
```

---

## What Makes a Reframe Legitimate vs. Overclaiming

| Legitimate | Overclaiming |
|---|---|
| Using the JD's terminology for experience you have | Adding tools/technologies you didn't use |
| Quantifying with estimates or ranges | Fabricating specific numbers |
| Emphasizing the business outcome of real technical work | Claiming ownership of work you contributed to |
| Surfacing scope that existed but wasn't stated | Inflating team size or user scale |
| Connecting adjacent work with an explicit bridge | Treating adjacent work as direct experience |

When in doubt: flag it as "not evidenced at the required level — recommend addressing in cover letter" rather than forcing a reframe.
