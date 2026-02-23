# portfolio
Enterprise automation tools and AI agents for Incident Management

# Olivia Keiter — Support Escalation Manager & Automation Engineer

> Building enterprise-grade tools that reduce toil, enforce consistency, and give Incident Managers their time back.

📍 Petersburgh, NY | Support Escalation Manager | Python · AI Integration · M365 Copilot Extensibility

https://www.linkedin.com/in/oliviakeiter/
olivia.j.keiter@outlook.com

---

## About

I'm a Support Escalation Manager who builds the tools my team actually needs. My work sits at the intersection of enterprise process design, Python automation, and AI agent development, turning hours of manual work into systems that run in minutes.

This repository showcases production tools and AI agents built to solve real operational challenges: reducing case review time by 95%, triaging email risk with zero guesswork, and unifying fragmented Incident Management workflows into a single intelligent assistant.

---

## Featured Projects

### Case Review Automation V5
**`Python · Pandas · OpenPyXL · Regex · AI Prompt Engineering`**

An enterprise automation pipeline that reduces weekly case review from 4-6 hours to 15 minutes — a **95% time reduction** saving an estimated **299 hours annually**.

**The problem:** Support Escalation Managers review 30+ account cases weekly. Manual review was slow, inconsistent, and impossible to scale.

**The solution:** A two-stage Python pipeline that auto-detects multi-format enterprise data exports, maps schemas dynamically, injects AI prompt templates, parses AI-generated summaries via regex, and produces formatted Excel reports with customer breakouts — all with a looping menu interface built for non-technical users.

| Metric | Result |
|---|---|
| Time per review session | 15 minutes (down from 4-6 hours) |
| Annual time saved | 299 hours |
| Cases processed | 40-50 per run |
| Escalation consistency | 100% |

**Technical highlights:**
- Multi-format detection: handles real `.xlsx`, HTML-as-xlsx, and CSV exports from different enterprise systems
- Fallback file reading across multiple encodings (`utf-8`, `latin-1`, `cp1252`, `iso-8859-1`)
- Dynamic column mapping between incompatible enterprise system schemas
- Smart column visibility: 11 key fields shown, all data preserved and hidden via OpenPyXL
- Tiered escalation logic: `AT RISK` (approaching threshold) and `Escalation Required` (threshold exceeded)
- Numbered output folders prevent overwrites and create a full audit trail
- 4 specialized AI prompt templates for different review types

**- User experience and personality**
The tool is designed to be used by real people under real time pressure — so it has a personality.
Loading screens and the AI processing stage (the longest wait in the pipeline) surface rotating tips. Some are practical IM guidance. Some are not: "In the morning, put on one sock at a time." The tips exist because waiting is less frustrating when something makes you smile.
At the end of every run, a "Tip Your Developer Jar" prompt lets users select a donation amount. The tool responds: "Just kidding, this tool is FREE!" and loops back to the home menu.
After 1,000 cases processed, the tool unlocks a game of Snake and a personalized breakdown of exactly how much time the user has saved through automation. It's a small thing. It's also the kind of thing people remember and talk about.
The philosophy: enterprise tooling doesn't have to feel like enterprise tooling. People use tools they enjoy using. Tools they enjoy using get adopted. Adoption is what creates the 299 hours of savings — not the code alone.

```
# Install
pip install pandas openpyxl lxml html5lib

# Run
python run.bat
# Stage 1: Data → AI Input
# [Process with AI platform]
# Stage 2: AI Output → Excel Reports
```

---

### IM OneStopShop
**`M365 Copilot · Agent Builder · Prompt Engineering · Enterprise Workflow Design`**

A unified M365 Copilot agent that consolidates five distinct Incident Management workflows into one interface. Users never need to think about which tool or agent to use — they just ask.

**The problem:** Incident Managers context-switched between multiple agents and tools to triage emails, review cases, monitor incidents, generate reports, and track long-running cases between multiple customers.

**The solution:** A single-entry-point agent that silently classifies each request into the correct internal workflow, applies the authoritative instruction set for that workflow, and returns production-ready output — with zero internal narration or routing logic exposed to the user.

**Workflows unified:**
- **Email Triage** - Full inbox triage grouped by Tracking ID, risk-stratified (HIGH/MEDIUM/LOW), with SLA logic and corporate action-required detection
- **Case Review** - Internal case review tables with cadence evaluation, high-risk flagging, and evidence-separated output
- **Long-Running Case (LRC) Monitoring** - Case registration, aging detection, escalation notices, dashboard summaries
- **Reactive Support Summary Generation** - Customer-facing Value-Based Delivery recommendation documents derived from Reactive Support Summaries.
- **Service Incident Monitoring** - ServiceNow incident triage, SLA breach detection, next-best-action proposals

**Design principles:** No internal narration. No routing disclosure. All work is completed in the current turn. One clarifying question maximum.

---

## Additional Agents

### Support Escalation Compass
Email triage agent for Incident Managers. Automatically reviews all unread support emails, groups by case (ID), applies strict SLA and engineering response window logic, and surfaces only the threads requiring IM intervention. Keeps IMs out of engineering's lane while ensuring nothing slips.

Key behaviors: corporate action-required emails always flagged HIGH RISK; sentiment + blocker + stakeholder data on every flagged item; SLA breach logic tied to severity windows.

---

### Olivia's Case Review Agent
Specialized case review assistant. Produces a single combined markdown table from Outlook, Teams case chats, and uploaded files — with cadence evaluation (Sev 2: daily, Sev 3: every 3 business days), high-risk logic, and all source evidence strictly separated into a dedicated section. Never guesses or infers facts not in the data. - Built with Buildy Buddy

---

### Buildy Buddy
A meta-agent that interviews Incident Managers and builds their own Case Review Assistant agent inside M365 Copilot Agent Builder. Walks through a 10-phase structured process: goal definition, customer scoping, data sources, output format, severity cadence rules, style guide, knowledge sources, instruction block generation, build steps, and testing iteration. Includes a custom icon creation phase on completion.

---

### LRC Guardian
Long-running case tracker. Registers cases, detects inactivity, generates dashboard-style summaries (active, overdue, escalated, resolved), drafts escalation notices, and recommends concrete next actions for stalled cases.

---

### Reactive Support Summary Generator
Generates customer-ready Word documents from Reactive Support Summary screenshots. Extracts product case distribution, infers dominant incident drivers, selects up to 3 Value-Based Delivery recommendations, and produces a formatted `.docx` with the screenshot embedded — ready to QA and share.

---

### Time Tracker
A natural-language time logging agent for Teams. Accepts short commands like `"add 30 for contract ID #### case review"`, maintains an in-session ledger, and generates an end-of-day summary grouped by customer and entry type with rounding to the nearest 15 minutes. Session-scoped by design — each day starts fresh.

---

## Skills Demonstrated

**Python Development**
Object-oriented design, file I/O, data structures, modular architecture, command-line UX

**Data Engineering**
Pandas DataFrames, multi-format detection, dynamic schema mapping, CSV/Excel manipulation, encoding handling, regex parsing

**AI Integration**
Prompt template design, bulk AI processing pipelines, response parsing and validation, quality control logic

**Enterprise Automation**
Two-stage pipeline architecture, tiered escalation logic, audit trail design, version-controlled outputs

**M365 Copilot Extensibility**
Agent Builder instruction design, multi-workflow classification, enterprise knowledge source integration, SLA and cadence logic

**Process Design**
Requirements gathering from business stakeholders, iterative development from V1 to V5, user-centric error handling, scalable architecture

---

## Contact

https://www.linkedin.com/in/oliviakeiter/
olivia.j.keiter@outlook.com

Open to discussing process automation strategies, Python development, AI integration in enterprise workflows, and M365 Copilot extensibility solutions.

*All sensitive enterprise information, customer data, and proprietary system names have been sanitized for public sharing.*
