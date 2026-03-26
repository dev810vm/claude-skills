# Claude Skills — Job Search Toolkit

A collection of Claude Code skills for job seekers. Drop these into Claude and get AI-powered resume review, company research, and application strategy — without copy-pasting into a chat window.

---

## Skills

| Skill | What it does |
|---|---|
| [resume-review](./resume-review/) | Scores your resume against a job description, flags gaps, and gives you a prioritized fix list |
| [company-intel](./company-intel/) | Researches a company and tells you what to mention in your cover letter and resume |

---

## Installation

Copy the skills to your Claude global skills directory:

```bash
cp -r company-intel ~/.claude/skills/
cp -r resume-review ~/.claude/skills/
```

That's it. The skills are available in any Claude Code session immediately.

---

## Quick Start

**Review a resume against a job posting:**
1. Put your resume and job description in the same folder (PDF, DOCX, or TXT — any readable format)
2. Open Claude Code in that folder
3. Say: `review my resume` or `how well does my resume match this job`

**Research a company before applying:**
1. Open Claude Code
2. Say: `research [Company Name]` or paste the job description and say `research this company`

---

## How It Works

These are [Claude Code skills](https://docs.anthropic.com/claude-code) — markdown files that give Claude a detailed set of instructions for a specific task. When you trigger a skill, Claude follows those instructions using its built-in tools (web search, file reading, etc.).

The skills are designed to:
- **Auto-detect files** in your current directory — no need to specify file paths
- **Run research in parallel** — web searches fire simultaneously to keep things fast
- **Save output to files** — results are written to your working directory so you can refer back to them

---

## Output Files

| Skill | Output file |
|---|---|
| resume-review | `[resume-name]-review-[company]-v1.md` (versioned — reruns create v2, v3, etc.) |
| company-intel | `intel-brief.md` |

---

## Tips

- **Run company-intel first** — if you run resume-review and an `intel-brief.md` already exists in the folder, it will use that instead of re-running the research, saving significant time
- **Add a cover letter** — put it in the same folder as your resume; resume-review will factor it into gap analysis
- **Rerun after edits** — resume-review is versioned, so rerunning after you update your resume creates a new report and shows you what improved
- **Multiple resume versions** — if you have more than one resume file in the folder, the skill reads all of them and treats the differences as context for the review
