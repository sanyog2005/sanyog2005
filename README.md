<a id="test-anchor"></a>
## Test Section


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

> 📊 **10 active roles** across 7 categories
> Last updated: May 08, 2026

## 📑 Quick Navigation

Jump to any role category:

### Main Roles

- [✍️ Technical Writing & Documentation](#technical-writing-documentation) (1 jobs)
- [📦 Product Marketing](#product-marketing) (2 jobs)
- [📈 Head of Growth](#head-of-growth) (7 jobs)

### Y Combinator Jobs


---

## ✍️ Technical Writing & Documentation

| Role | Company | Location | Apply |
|------|---------|----------|-------|
| Technical Writer & Product Engineer | Thermal Works | United States | [→](https://remoteOK.com/remote-jobs/remote-technical-writer-product-engineer-thermal-works-1131481) |


[⬆ Back to top](#-quick-navigation)

---

## 📦 Product Marketing

| Role | Company | Location | Apply |
|------|---------|----------|-------|
| Product Marketing Intern | Everlaw | Oakland | [→](https://remoteOK.com/remote-jobs/remote-product-marketing-intern-everlaw-1131454) |
| Product Marketing Lead | Paragon | Los Angeles or Remote | [→](https://remoteOK.com/remote-jobs/remote-product-marketing-lead-paragon-1131395) |


[⬆ Back to top](#-quick-navigation)

---

## 📈 Head of Growth

| Role | Company | Location | Apply |
|------|---------|----------|-------|
| Senior Veritas eDiscovery Platform Engineer | Contact Government Services, LLC | Remote | [→](https://remoteOK.com/remote-jobs/remote-senior-veritas-ediscovery-platform-engineer-contact-government-services-llc-1131484) |
| Medical Affairs Solutions Manager UK | Sorcero | UK | [→](https://remoteOK.com/remote-jobs/remote-medical-affairs-solutions-manager-uk-sorcero-1131475) |
| Recruiter | Airship | Remote - U.S. | [→](https://remoteOK.com/remote-jobs/remote-recruiter-airship-1131462) |
| Social Media Growth Lead | Black &amp; White Zebra | Remote | [→](https://remoteOK.com/remote-jobs/remote-social-media-growth-lead-black-amp-white-zebra-1131434) |
| Supply Chain Manager | Nutrafol | Remote | [→](https://remoteOK.com/remote-jobs/remote-supply-chain-manager-nutrafol-1131406) |
| Strategic Business Development Consultant | Vonage | Spain | [→](https://remoteOK.com/remote-jobs/remote-strategic-business-development-consultant-vonage-1131403) |
| Manager Client Support RH Boutique Partners | Waterworks | Remote | [→](https://remoteOK.com/remote-jobs/remote-manager-client-support-rh-boutique-partners-waterworks-1131392) |


[⬆ Back to top](#-quick-navigation)

---

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

**Example output:**
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


[Click to go to test](#test-anchor)

**Example output:**
