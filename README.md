# Developer Marketing Jobs
![Jobs](https://img.shields.io/badge/🧑‍💻_Jobs-Updated_Daily-brightgreen?style=for-the-badge)
![Free](https://img.shields.io/badge/💸_Access-100%25_Free-blue?style=for-the-badge)
![No Signup](https://img.shields.io/badge/🔓_No_Signup-Required-orange?style=for-the-badge)
![Powered By](https://img.shields.io/badge/⚡_Powered_By-GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Banner GIF](https://infrasity-pull-zone.b-cdn.net/ReadmeGif.gif)

**Every open Developer Advocate DevRel, technical writing, developer marketing, community, and docs role at devtool companies — in one place.**

Curated nightly. Pulled directly from company ATS feeds. No reposts, no aggregator noise.

[![Updated daily](https://img.shields.io/badge/updated-daily-brightgreen)](#)
[![Jobs tracked](https://img.shields.io/badge/jobs-tracked%20daily-7B6BFF)](#)
[![Maintained by Infrasity](https://img.shields.io/badge/maintained%20by-Infrasity-7B6BFF)](https://infrasity.com)

---

## Why this exists

DevRel and technical writing roles are scattered across LinkedIn, careers pages, niche newsletters, and Slack channels. Finding them takes hours. We pull them directly from each company's ATS every night so you don't have to.

If you're hiring, you can submit roles by [opening an issue](#submit-a-role).

---

<!-- JOBS:START -->
| Role | Company | Location | Source | Link |
|------|---------|----------|--------|------|
| AI Staff Developer Advocate | Mongodb | California; San Francisco | Greenhouse | [Apply](https://www.mongodb.com/careers/job/?gh_jid=7673691) |
| Senior Developer Advocate | Mongodb | Ireland | Greenhouse | [Apply](https://www.mongodb.com/careers/job/?gh_jid=7241758) |
| Staff Developer Advocate | Mongodb | New York | Greenhouse | [Apply](https://www.mongodb.com/careers/job/?gh_jid=7831638) |
| Technical Writer | Mongodb | Dublin | Greenhouse | [Apply](https://www.mongodb.com/careers/job/?gh_jid=7743754) |
| Technical Writer & Product Engineer | Thermal Works | United States | RemoteOK | [Apply](https://remoteOK.com/remote-jobs/remote-technical-writer-product-engineer-thermal-works-1131481) |
| Senior Software Engineer - Docs Engineering - Documentation | Elastic | Spain | Greenhouse | [Apply](https://jobs.elastic.co/jobs?gh_jid=7893106&gh_jid=7893106) |
| Writer, Content Marketing | Stripe | Remote US | Greenhouse | [Apply](https://stripe.com/jobs/search?gh_jid=7587814) |
| Sales Content Manager | Figma | San Francisco, CA • New York, NY • United States | Greenhouse | [Apply](https://boards.greenhouse.io/figma/jobs/5985022004?gh_jid=5985022004) |
| Senior Developer Advocate | Elastic | The Netherlands | Greenhouse | [Apply](https://jobs.elastic.co/jobs?gh_jid=7445210&gh_jid=7445210) |
| Senior Developer Advocate (Video Content Creator) | Elastic | United Kingdom | Greenhouse | [Apply](https://jobs.elastic.co/jobs?gh_jid=7190130&gh_jid=7190130) |
| Content Marketing Intern (July to December 2026) | Cloudflare | In-Office | Greenhouse | [Apply](https://boards.greenhouse.io/cloudflare/jobs/7733168?gh_jid=7733168) |
| Content Marketing Intern (Summer 2026) | Cloudflare | In-Office | Greenhouse | [Apply](https://boards.greenhouse.io/cloudflare/jobs/7733145?gh_jid=7733145) |
| Developer Advocate | Figma | San Francisco, CA | Greenhouse | [Apply](https://boards.greenhouse.io/figma/jobs/5834922004?gh_jid=5834922004) |
| Developer Advocate (Tokyo, Japan) | Figma | Tokyo, Japan | Greenhouse | [Apply](https://boards.greenhouse.io/figma/jobs/5969647004?gh_jid=5969647004) |
| Sr. Developer Advocate - Neon | Databricks | San Francisco, California | Greenhouse | [Apply](https://databricks.com/company/careers/open-positions/job?gh_jid=8428818002) |
| Sr. Developer Advocate, Databricks AI Agentic Systems | Databricks | San Francisco, California | Greenhouse | [Apply](https://databricks.com/company/careers/open-positions/job?gh_jid=7930603002) |
| Senior Frontend Developer | Sanctuary Computer | LATAM, Asia | Remotive | [Apply](https://remotive.com/remote-jobs/software-development/senior-frontend-developer-2088707) |
| Fullstack Developer (US - ET) | Chooose | USA | Remotive | [Apply](https://remotive.com/remote-jobs/software-development/fullstack-developer-us-et-2088706) |

_Last updated: 2026-05-08 07:47 UTC_
<!-- JOBS:END -->

---

**Showing the freshest 100 jobs across all categories.**

---

## How it works

This repo runs a nightly script that:

1. Reads company ATS feeds (Greenhouse, Lever, Ashby, Workable)
2. Filters by role keywords (DevRel, advocate, technical writer, community, developer marketing, docs)
3. Rebuilds this README with fresh jobs every day

**Sources:** Greenhouse · Lever · Ashby · Workable · YC · RemoteOK · Remotive · Arbeitnow · Adzuna

**No scraping. No reposts. No LinkedIn dust.**

---

## 🤖 Claude Code Skills

This repo includes **Claude Code skills** that contributors can run locally to maintain and improve the project. Skills are markdown files that Claude reads and executes — they let anyone with Claude Code installed extend the project without writing code.

### Prerequisites

```bash
# Install Claude Code CLI
npm install -g @anthropic-ai/claude-code

# Login (uses your Claude Pro/Max subscription)
claude login
```

### Available Skills

#### 1. Expand Keywords (`skills/expand-keywords.md`)

Automatically expands the keyword lists in `main.py` for each job category. Currently each category has ~10 hardcoded keywords. This skill expands them to 30+ using Claude's knowledge of real job titles, including variations, seniority prefixes, and synonyms.

**When to use:**
- Jobs you expect to see aren't showing up in the README
- After adding a new category to `main.py`
- Monthly refresh (job titles evolve over time)

**How to run:**

```bash
# From repo root
claude skills/expand-keywords.md
```

**What it does:**
- Reads current `CATEGORIES` from `main.py`
- For each category, generates 30+ additional job title keywords
- Merges new keywords with existing ones (no duplicates)
- Updates `main.py` directly
- Shows a summary of new keywords added

---

### Skill 2: Expand Greenhouse Companies

**File:** `skills/expand-greenhouse-companies.md`

Auto-discovers new devtool companies using Greenhouse ATS. The Greenhouse API requires company names as parameters — this skill expands the company list automatically instead of hardcoding it.

**When to use:**
- Monthly refresh to discover new companies
- When a specific company is missing from job listings
- After major tech hiring waves
- When `greenhouse_jobs.json` seems low on results

**How to run:**
```bash
claude skills/expand-greenhouse-companies.md
```

**What it does:**
- Reads current company list from `fetchers/greenhouse.py`
- Generates 200+ candidate devtool companies based on industry knowledge
- Validates each against the Greenhouse API in real-time
- Filters for actual devtool/SaaS companies
- Updates `fetchers/greenhouse.py` directly
- Updates `discovered_greenhouse_companies.json` cache

