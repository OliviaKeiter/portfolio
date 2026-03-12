# Enterprise AI Agent Portfolio

**Olivia Keiter — Support Escalation Manager & Automation Engineer**

Building enterprise-grade AI agents and automation tools that reduce toil, enforce consistency, and give Incident Managers their time back.

📍 Petersburgh, NY | Support Escalation Manager | Python · Azure AI · M365 Copilot Extensibility · LLM Orchestration

[![LinkedIn](https://img.shields.io/badge/LinkedIn-oliviakeiter-blue)](https://www.linkedin.com/in/oliviakeiter/)
[![Email](https://img.shields.io/badge/Email-olivia.j.keiter%40outlook.com-lightgrey)](mailto:olivia.j.keiter@outlook.com)

---

## About

I'm a Support Escalation Manager who builds the tools my team actually needs.

My work sits at the intersection of enterprise process design, Python automation, and AI agent development -- turning hours of manual work into systems that run in minutes. Everything in this repository was built to solve a real operational problem in a live federal enterprise environment supporting 30+ U.S. Government customers.

This portfolio spans two layers of work:

- **Python automation pipelines** -- data engineering, AI integration, and enterprise reporting tools
- **M365 Copilot AI agents** -- production agents with full instruction sets, SLA logic, escalation guardrails, and governance controls

The result: an interconnected ecosystem of 9 agents and tools that collectively eliminate approximately 1,000 manual actions per day, reduce case review time by 95%, and give Incident Managers a single intelligent interface for every workflow they touch.

---

## Featured Projects

### Incident Management Hub (IMHub) v1.1
`Python` `Azure AI` `M365 Copilot` `LLM Orchestration` `Prompt Engineering`

The flagship project. IMHub is a full agentic incident management platform built and deployed in a federal enterprise environment. It evolved from the Case Review Automation pipeline into a multi-stage AI system that handles triage, escalation routing, executive reporting, and risk prioritization at scale.

**Impact:** Eliminates approximately 1,000 manual actions per day. Enabled daily case reviews across 30+ government accounts at a scale previously impossible with manual methods.

**Features:**
- Multi-stage AI pipeline with LLM orchestration
- Executive PDF reporting with AI-generated summaries
- Trend tracking and visual charts
- Parent-child case relationship handling
- Closed case processing for after-action reviews
- Session restore and audit logging
- Integrated feedback form and bug detection with IcM tracking

---

### Case Review Automation V1
`Python` `Pandas` `OpenPyXL` `Regex` `AI Prompt Engineering`

The origin of IMHub. A two-stage enterprise automation pipeline that reduces weekly case review from 4-6 hours to 15 minutes -- an estimated 95% time reduction, saving approximately 299 hours annually.

**The problem:** Support Escalation Managers review 30+ account cases weekly. Manual review was slow, inconsistent, and impossible to scale.

**The solution:** A two-stage Python pipeline that auto-detects multi-format enterprise data exports, maps schemas dynamically, injects AI prompt templates, parses AI-generated summaries, and produces formatted Excel reports with customer breakouts -- all through a looping menu interface built for non-technical users.

| Metric | Result |
|---|---|
| Time per review session | 15 minutes (down from 4-6 hours) |
| Annual time saved | ~299 hours |
| Cases processed per run | 40-50 |
| Escalation consistency | 100% |

**Technical highlights:**
- Multi-format detection: handles .xlsx, HTML-as-xlsx, and CSV exports from different enterprise systems
- Fallback file reading across multiple encodings (utf-8, latin-1, cp1252, iso-8859-1)
- Dynamic column mapping between incompatible enterprise system schemas
- Tiered escalation logic: AT RISK (approaching threshold) and Escalation Required (threshold exceeded)
- Numbered output folders prevent overwrites and create a full audit trail
- 4 specialized AI prompt templates for different review types

**On the user experience:** This tool is built for real people under real time pressure, so it has a personality. Loading screens surface rotating tips -- some practical IM guidance, some not ("In the morning, put on one sock at a time."). After 1,000 cases processed, the tool unlocks a game of Snake and a personalized breakdown of exactly how much time the user has saved. At the end of every run, a Tip Your Developer Jar prompt lets users select a donation amount. The tool responds: "Just kidding, this tool is FREE!"

The philosophy: enterprise tooling doesn't have to feel like enterprise tooling. People use tools they enjoy. Tools they enjoy get adopted. Adoption is what creates the 299 hours of savings -- not the code alone.

```bash
pip install pandas openpyxl lxml html5lib
python run.bat
```

---

## M365 Copilot Agent Ecosystem

The agents below were designed, built, and deployed independently inside M365 Copilot Agent Builder. Each solves a specific operational problem. Together they form a unified system -- all accessible through a single entry-point agent (IM OneStopShop) so operators never have to think about which tool to use.

All agents include full instruction sets with guardrails, edge case handling, SLA logic, and compliance controls baked in. These are not demos or prototypes. They run in production.

---

### IM OneStopShop
`M365 Copilot` `Agent Builder` `Multi-Workflow Classification` `Enterprise Workflow Design`

A unified meta-agent that consolidates five distinct Incident Management workflows into one interface. Users never need to think about which tool or agent to use -- they just ask.

**The problem:** Incident Managers context-switched between multiple agents and tools to triage emails, review cases, monitor incidents, generate reports, and track long-running cases.

**The solution:** A single-entry-point agent that silently classifies each request into the correct internal workflow, applies the authoritative instruction set for that workflow, and returns production-ready output -- with zero internal narration or routing logic exposed to the user.

**Workflows unified:**
- Email Triage -- full inbox triage grouped by Tracking ID, risk-stratified (HIGH/MEDIUM/LOW), with SLA logic and corporate action-required detection
- Case Review -- internal case review tables with cadence evaluation, high-risk flagging, and evidence-separated output
- Long-Running Case (LRC) Monitoring -- case registration, aging detection, escalation notices, dashboard summaries
- RSPR Generation -- customer-facing Value-Based Delivery recommendation documents from Reactive Support Summary data
- Service Incident Monitoring -- ServiceNow and IcM incident triage, SLA breach detection, next-best-action proposals

**Design principles:** No internal narration. No routing disclosure. All work completed in the current turn. One clarifying question maximum.

---

### IM Compass (Support Escalation Compass)
`M365 Copilot` `Agent Builder` `SLA Logic` `Email Triage` `Risk Stratification`

Intelligent email triage agent for Incident Managers. Automatically reviews all unread support emails, groups by case (Tracking ID), applies strict SLA and engineering response window logic, and surfaces only the threads requiring IM intervention -- keeping IMs out of engineering's lane while ensuring nothing slips.

**Key behaviors:**
- Triages all unread support and non-support emails without prompting
- Groups output by Tracking ID, not individual email
- Risk stratification: HIGH / MEDIUM / LOW / NOT FLAGGED / NON-SUPPORT UPDATES
- Corporate action-required emails (access at risk, compliance notices, required training) always flagged HIGH RISK
- Enforces engineering SLA windows -- never escalates inside Sev A 4hr or Sev B 24hr windows unless frustration, blockers, or escalation intent are present
- Every flagged item includes: agency name, Tracking ID, sentiment with timestamp, blockers, stakeholders, and one-sentence recommended IM action

---

### Olivia's Case Review Agent
`M365 Copilot` `Agent Builder` `Grounded AI` `Cadence Logic` `Evidence Governance`

Specialized case review assistant. Produces a single combined markdown table from Outlook, Teams case chats, and uploaded files -- with cadence evaluation, high-risk logic, and all source evidence strictly separated.

**Key behaviors:**
- Sources: Outlook primary inbox, Teams case-specific chats, and manually uploaded Excel/CSV files only
- Never guesses, infers, or fabricates facts not present in the data
- Cadence evaluation: Sev B requires daily business-day updates; Sev C requires updates every 3 business days
- High-risk flagging when: case is out of cadence, customer escalates, sentiment is clearly negative, or IM involvement is requested in Teams
- All raw source evidence appears in a dedicated Source Excerpts section -- never inside the case table
- Built using Buildy Buddy (see below)

**Table columns (fixed order):** Case number, Case summary, Customer impact and sentiment, Current status, Latest customer communications, Latest internal notes, Blockers and dependencies, IM attention needed or high risk, Product or workload, Agency

---

### Buildy Buddy
`M365 Copilot` `Agent Builder` `Meta-Agent` `Prompt Engineering` `Iterative Development`

A meta-agent that interviews Incident Managers and builds their own Case Review Assistant agent inside M365 Copilot Agent Builder. The output is a custom, fully configured agent tailored to that IM's specific customers, review style, and communications cadence.

**10-phase structured process:**
1. Goal and boundaries
2. Customer scoping and segmentation
3. Input data sources
4. Case review output format definition
5. Severity and cadence rules
6. Style guide (dates, time zones, tone, abbreviations)
7. Knowledge sources to connect
8. Auto-generated instruction block (ready to paste into Agent Builder)
9. Step-by-step build guidance in M365 Copilot
10. Testing plan and iteration loop -- requires real conversation threads before sign-off

**Completion criteria:** The new agent must have knowledge sources connected, file creation enabled, image generation enabled, and at least one real iteration based on test conversation threads before Buildy Buddy considers the build done.

**Bonus:** On completion, Buildy Buddy prompts the IM to design a custom icon for their new agent and guides them through the image creation and upload process.

---

### Service Incident Agent
`M365 Copilot` `Agent Builder` `ServiceNow` `IcM` `SLA Monitoring` `RBAC`

Incident monitoring agent scoped to the US GCC space. Monitors ServiceNow, IcM, and Iridis for active outages and incidents, detects SLA breaches and missing-update violations, and proposes next best actions.

**Key behaviors:**
- Retrieves and summarizes incidents by severity, service, product, technology, time window, and affected customers
- Detects SLA risks (approaching or breached) and missing-update breaches (no work notes in X hours)
- Always cites ticket IDs, timestamps, and owners -- never fabricates states or ownership
- RBAC-safe: never reveals data the caller is not permitted to see
- When tool calls fail, reports the failure and proposes a manual fallback
- Proposes next best actions when asked; calls appropriate Power Automate flows when acting

---

### RSPR Generator (Reactive Support Summary Generator)
`M365 Copilot` `Agent Builder` `Document Generation` `Data Extraction` `Customer-Facing Output`

Generates customer-ready Word documents from Reactive Support Summary screenshots or structured inputs. Extracts product case distribution, infers dominant incident drivers, selects up to 3 Value-Based Delivery (VBD) recommendations, and produces a formatted .docx with the screenshot embedded -- ready to QA and share.

**Key behaviors:**
- Screenshot-first: when screenshots are provided, they are the system of record
- Extracts reporting month, product family case counts, and customer name from visible data only -- never guesses missing values
- Identifies primary problem areas using a co-primary rule: products within 10% of the top case count are treated as co-primary
- Applies a VBD suitability gate: each recommendation must directly address the inferred incident driver, match the product scope, and plausibly improve outcomes within 30-90 days
- Generates the Word document immediately when data is sufficient -- no unnecessary confirmation loops
- Output includes: case summary, VBD recommendations (max 3 sentences each), closing statement mapping VBDs to operational outcomes, and supporting screenshots in an appendix

---

### LRC Guardian
`M365 Copilot` `Agent Builder` `Case Tracking` `Escalation Logic` `Dashboard Generation`

Long-running case tracker. Registers cases, detects inactivity, generates dashboard-style summaries, drafts escalation notices, and recommends concrete next actions for stalled cases.

**Key behaviors:**
- Case registration with age tracking (days since open)
- Inactivity detection and risk flagging
- Dashboard summaries: active, overdue, escalated, resolved
- Drafts escalation notices and customer-safe updates on request
- Recommends specific next actions to progress stalled cases
- Treats "case," "SR," and "ticket" as interchangeable

---

### Time Tracker
`M365 Copilot` `Agent Builder` `Natural Language Processing` `Time Logging` `Teams`

Natural-language time logging agent for Teams. Accepts short commands, maintains an in-session ledger, and generates an end-of-day summary grouped by customer and entry type with rounding to the nearest 15 minutes. Session-scoped by design -- each day starts fresh in a new chat.

**Supported commands:**
```
"add 30 for DOC package 4321 case review"
"add 45 for account communications for Contoso, package 7788, notes follow-up call"
"remove 15 for DOC case review"
"show my entries"
"daily summary"
```

**Key behaviors:**
- Accepts customer, package ID, entry type, minutes, and optional notes in any natural phrasing
- Entry types: Case Review, Admin, Case Escalation, Account Communications, Other
- Never guesses customers, package IDs, or time durations
- Removals recorded as negative adjustments -- no entries are deleted
- Rounding applied only at summary time, not during entry logging
- Mandatory close-out message at end of every summary: start a new chat to begin a fresh day

---

## Skills Demonstrated

| Area | Details |
|---|---|
| Python Development | Object-oriented design, file I/O, data structures, modular architecture, command-line UX |
| Data Engineering | Pandas DataFrames, multi-format detection, dynamic schema mapping, CSV/Excel manipulation, encoding handling, regex parsing |
| AI Integration | Prompt template design, bulk AI processing pipelines, LLM orchestration, response parsing and validation |
| Enterprise Automation | Two-stage pipeline architecture, tiered escalation logic, audit trail design, version-controlled outputs |
| M365 Copilot Extensibility | Agent Builder instruction design, multi-workflow classification, SLA and cadence logic, enterprise knowledge source integration |
| Agent Architecture | Guardrail design, edge case handling, RBAC-aware outputs, human-in-the-loop governance, meta-agent orchestration |
| Process Design | Requirements gathering from business stakeholders, iterative development, user-centric error handling, scalable architecture |

---

## Certifications

- AI-900 | Azure AI Fundamentals | March 2026
- AZ-900 | Microsoft Azure Fundamentals | January 2022
- SC-900 | Microsoft Security, Compliance, and Identity Fundamentals | May 2022

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-oliviakeiter-blue)](https://www.linkedin.com/in/oliviakeiter/)
[![Email](https://img.shields.io/badge/Email-olivia.j.keiter%40outlook.com-lightgrey)](mailto:olivia.j.keiter@outlook.com)

Open to discussing process automation, AI agent development, enterprise workflow design, and M365 Copilot extensibility solutions.

---

*All sensitive enterprise information, customer data, and proprietary system names have been sanitized for public sharing.*


