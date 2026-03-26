# Scoring Rubric — Resume Review Skill

Detailed criteria for scoring each of the five evaluation dimensions. Weights vary by role archetype — see the main skill for the three weight sets (IC Technical, People Leadership, Cross-Functional).

---

## 1. Technical Skills

Score based on how many required and preferred technical skills are evidenced in the resume.

| Score Range | Criteria |
|---|---|
| 90–100% | All required technical skills present; most preferred skills present |
| 75–89% | All required skills present; some preferred skills missing |
| 60–74% | Most required skills present; 1–2 required gaps |
| 40–59% | Several required skills missing; significant gaps |
| 0–39% | Core technical requirements largely unmet |

**Scoring notes:**
- Give partial credit for adjacent skills (e.g., PostgreSQL experience when MySQL is required: 70–80% credit)
- Give partial credit for older or non-primary experience with a required tool
- A skill listed in a skills section with no context gets less weight than one evidenced in work experience
- Distinguish between "must-have" and "nice-to-have" skills in the JD when scoring gaps

---

## 2. Experience & Seniority

Evaluate whether the candidate's experience level, career trajectory, and work history match the role requirements.

| Score Range | Criteria |
|---|---|
| 90–100% | Years of experience meet/exceed requirement; seniority level matches; relevant responsibilities align closely; clear upward trajectory |
| 75–89% | Close match on years; role level aligns; minor gaps in specific responsibilities |
| 60–74% | Slightly under on years OR role scope is one level below target |
| 40–59% | Noticeably under-experienced (e.g., 3 years for a role requiring 6) OR significant scope gap |
| 0–39% | Substantially under-qualified on experience; clear mismatch in seniority |

**Seniority level calibration (typical):**
- Entry/Junior: 0–2 years
- Mid-level: 2–5 years
- Senior: 5–10 years
- Staff/Principal/Lead: 8+ years with demonstrated leadership/scope
- Director/VP: management experience required

**Scoring notes:**
- Total years in adjacent roles can count toward experience, not just exact title matches
- Scope matters: a PM at a 5-person startup vs. a Fortune 500 are different seniority signals
- Career progression (promotions, expanding scope) is a strong positive signal — prioritize trajectory over raw years
- Job hopping (<1 year at multiple consecutive roles) reduces this score; contract/agency work is an exception
- Unexplained employment gaps >6 months reduce this score unless context is clear (caregiving, education, layoff)

---

## 3. Domain Knowledge

Assess familiarity with the industry, product area, or functional domain the role requires.

| Score Range | Criteria |
|---|---|
| 90–100% | Direct industry/domain experience; deep functional expertise matches JD closely |
| 75–89% | Strong related domain experience with transferable knowledge |
| 60–74% | Adjacent domain experience; some transferable knowledge |
| 40–59% | Tangentially related; significant ramp-up likely needed |
| 0–39% | No evident domain overlap |

**Domain categories to consider:**
- Industry vertical (fintech, healthcare, e-commerce, SaaS, etc.)
- Product area (payments, auth, search, recommendation systems, etc.)
- Functional discipline (growth, platform, infra, ML, security, etc.)
- Customer type (B2B, B2C, enterprise, SMB, consumer)
- Company stage (startup, growth, enterprise)

---

## 4. Education & Credentials

Compare stated educational requirements and certifications against the resume.

| Score Range | Criteria |
|---|---|
| 90–100% | Meets degree requirement; holds relevant certifications if required |
| 75–89% | Meets degree requirement; missing preferred (not required) certifications |
| 60–74% | Degree is in a related but not exact field; or has equivalent demonstrated experience |
| 40–59% | Degree requirement not met but has substantial compensating experience |
| 0–39% | Hard degree/credential requirement clearly not met; no evident compensating factors |

**Notes:**
- Many JDs state "or equivalent experience" — if the candidate has strong relevant experience, this should be treated as meeting the requirement
- Certifications that are "required" vs. "preferred" should be weighted accordingly
- For technical roles, demonstrated skills often outweigh formal credentials
- If the JD does not specify educational requirements, score this dimension at 85% by default

---

## 5. Soft Skills & Culture Fit

Evaluate signals for the interpersonal and cultural attributes the JD emphasizes.

| Score Range | Criteria |
|---|---|
| 90–100% | Strong explicit evidence of stated soft skills (e.g., cross-functional leadership described in bullets) |
| 75–89% | Good implicit evidence; soft skills evident from context and scope of work |
| 60–74% | Some signals present; some stated soft skill requirements not evidenced |
| 40–59% | Limited soft skill evidence; resume is purely technical with no collaboration signals |
| 0–39% | Resume actively contradicts stated cultural requirements |

**Common soft skill signals to look for:**
- Cross-functional collaboration: "worked with X, Y, Z teams", "partnered with"
- Leadership: "led", "managed", "mentored", "owned"
- Communication: presentations, writing, stakeholder management
- Autonomy/initiative: "founded", "spearheaded", "drove", "built from scratch"
- Adaptability: diverse roles, startup experience, rapid growth environments

---

## Overall Match Score Interpretation

| Score | Label | Recommended Action |
|---|---|---|
| 85–100% | Strong Match | Apply confidently; resume may need minor keyword tweaks |
| 70–84% | Good Match | Apply with targeted resume adjustments |
| 55–69% | Moderate Match | Address key gaps before applying; may still be worth trying |
| 40–54% | Weak Match | Significant gaps; consider if role is the right target |
| 0–39% | Poor Match | Fundamental misalignment; focus on different roles |

---

## ATS Keyword Scoring

When assessing keyword gaps, prioritize:

1. **High priority** — Exact phrases from the JD title, required skills, or repeated throughout JD
2. **Medium priority** — Tools/technologies mentioned once in requirements
3. **Low priority** — Soft skill words and general adjectives

Flag as an ATS risk if 3+ high-priority keywords from the JD are absent from the resume.

Target keyword match rate: **65–75%** to pass modern AI-powered ATS screening.

## ATS Formatting Failures (Instant Disqualifiers)

The following formatting choices cause ATS systems to misparse or reject resumes regardless of content quality:

| Issue | Why It Fails | Fix |
|---|---|---|
| Multi-column layout | ATS reads left-to-right, merges columns into garbled text | Single-column layout |
| Text boxes / shapes | Content inside not parsed as resume text | Move to body text |
| Tables for content layout | Cells often misread or skipped | Use plain bullet lists |
| Headers/footers with key info | Many parsers strip these entirely | Move to body |
| Graphics, icons, photos | Not readable; can corrupt surrounding text parsing | Remove |
| Uncommon fonts or Unicode symbols | May render as garbage characters | Use standard fonts, ASCII bullets |
| Non-standard section headings | "Career Journey" won't be recognized as "Work Experience" | Use conventional headings |

Note: Text-based PDF is now the recommended default for most modern ATS. Use `.docx` only if the posting explicitly requests it or the employer is known to use iCIMS or legacy Taleo.
