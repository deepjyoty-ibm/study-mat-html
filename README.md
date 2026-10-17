# 📚 Study Mat HTML — Technical Interview Study Guide

A structured, visually rich, self-contained HTML study guide system for technical interview preparation.
Each topic is authored as a **single HTML file** that can be opened directly in a browser, used for deep learning, and quickly revised the night before an interview.

---

## 🗂️ Project Structure

```
study-mat-html/
│
├── README.md                               ← You are here
│
├── docs/
│   ├── instructions.md                     ← Master prompt / authoring spec
│   ├── prompt.txt                          ← Utility prompt text
│   ├── master-prompts/
│   │   └── Any-Topic-Master-Question-List-Prompt.md   ← Template for generating question lists
│   └── study-questions/
│       └── Azure-Function-App-Master-Question-List.md ← Q1–Q49 source for Azure Functions
│
└── study-html/
    ├── assets/
    │   ├── css/
    │   │   └── blue-theme.css              ← Shared CSS (Blue theme, all components)
    │   └── images/                         ← (reserved for future diagrams/icons)
    │
    └── src/
        ├── templates/                      ← (reserved for future HTML templates)
        └── azure/
            └── azure-function-app/
                ├── Function-App-Complete-Notes.html         ← English version (Q1–Q49, 15 chapters)
                └── Function-App-Complete-Notes-Bengali.html ← Bengali version (Q1–Q49, 15 chapters)
```

---

## 📖 Available Study Guides

### ☁️ Azure Function App

| File | Language | Chapters | Questions | Status |
|------|----------|----------|-----------|--------|
| [`Function-App-Complete-Notes.html`](study-html/src/azure/azure-function-app/Function-App-Complete-Notes.html) | 🇬🇧 English | 15 + NBR | Q1–Q49 | ✅ Complete |
| [`Function-App-Complete-Notes-Bengali.html`](study-html/src/azure/azure-function-app/Function-App-Complete-Notes-Bengali.html) | 🇧🇩 Bengali | 15 + NBR | Q1–Q49 | ✅ Complete |

**Chapters covered:**
| # | Chapter | Key Topics |
|---|---------|------------|
| 01 | Azure Functions Fundamentals | Serverless, Function vs Function App, Isolated Worker |
| 02 | Azure Function Triggers | HTTP, Timer, Blob, Queue, Service Bus, Event Grid, Event Hub |
| 03 | .NET Isolated Worker Model | Program.cs, HostBuilder, DI, Middleware, FunctionContext |
| 04 | Configuration | local.settings.json, App Settings, Options Pattern, IConfiguration |
| 05 | Identity, Credentials & Secrets | Managed Identity, DefaultAzureCredential, Key Vault, RBAC |
| 06 | CORS & API Security | CORS, Preflight, Same-Origin Policy, Function Keys, Entra ID |
| 07 | Hosting, Scaling & Runtime | Consumption / Flex / Premium / Dedicated, Cold Start, Scale-Out |
| 08 | Networking | VNet Integration, Private Endpoint, Access Restrictions, Private DNS |
| 09 | Logging & Monitoring | ILogger, Structured Logging, Application Insights, CorrelationId |
| 10 | Deployment | dotnet publish, GitHub Actions, Deployment Slots, Zero-Downtime |
| 11 | Production-Ready Function App | Local→Production checklist |
| 12 | Tricky Interview Questions | Q27–Q36, deep-understanding answers |
| 13 | Scenario-Based Questions | Q37–Q43, real problems & solutions |
| 14 | Architecture-Level Questions | Q44–Q48, enterprise design decisions |
| 15 | Final Revision Question | Q49, complete one-shot mental map |
| NBR | Night-Before Interview Revision | Rapid sweep, traps, checklists, code patterns |

---

## 🎨 Design System

All HTML files share a single external CSS file: [`study-html/assets/css/blue-theme.css`](study-html/assets/css/blue-theme.css)

### Theme
- **Current:** Blue theme (`:root` CSS variables — easy to swap)
- **Planned:** Dark theme, High-contrast theme

### Components available in CSS
| Component | Class | Purpose |
|-----------|-------|---------|
| Chapter header | `.chapter-header`, `.ch-num`, `.ch-title` | Numbered chapter banners |
| Question block | `.question-block`, `.q-label`, `.q-text` | Interview question display |
| Callouts | `.callout-blue/green/orange/red/purple/yellow/gray` | Concept, tip, warning, architecture notes |
| Code blocks | `.code-block`, `.code-block-header` | VS Code dark theme syntax highlighting |
| Syntax spans | `.kw .tp .st .mt .vr .cm .nm .at` | Keyword, Type, String, Method, Var, Comment, Number, Attribute |
| Diagrams | `.diagram`, `.diagram-title` | ASCII architecture diagrams |
| Tables | `.compare-table` | Feature comparison tables |
| Flow steps | `.flow`, `.flow-step`, `.flow-box`, `.flow-arrow` | Step-by-step process flows |
| Revision box | `.revision-box` | Quick revision bullet lists |
| Two-column grid | `.grid-2` | Side-by-side callout pairs |
| NBR section | `.nbr-section` | Night-Before Revision (dark blue background) |
| Cover banner | `.cover-banner` | Title page hero section |
| TOC | `.toc-grid` | Table of contents grid |

---

## 🚀 How to Use

### View in Browser
Just open any HTML file directly in your browser — no server needed, no build step.

```
study-html/src/azure/azure-function-app/Function-App-Complete-Notes.html
```

### Convert to PDF
Open in Chrome → `Ctrl+P` → **Save as PDF**.
The CSS includes print styles (`@media print`) for clean PDF output.

---

## 🛠️ Adding a New Topic

1. Create a question list in `docs/study-questions/<Topic-Name>-Master-Question-List.md`
2. Use `docs/instructions.md` as the authoring spec
3. Create HTML file at `study-html/src/<cloud-or-category>/<topic-name>/<Topic>-Complete-Notes.html`
4. Link the shared CSS: `../../../assets/css/blue-theme.css`
5. Follow the same chapter/component structure

---

## 📦 Tech Stack

- **Pure HTML + CSS** — zero dependencies, zero build tools
- **External CSS only** — one theme file shared across all study guides
- **Bengali Unicode** — full Bengali script support for regional language notes
- **Self-contained** — open any file, it just works

---

## 📝 Authoring Notes

- `local.settings.json` is never committed (gitignored)
- Bengali version: question text stays in English, all explanations in Bengali, technical terms stay in English
- Code blocks use VS Code dark theme colour classes (not a library — pure CSS spans)
- Diagrams are ASCII art inside `<pre>` blocks — renders perfectly in any browser and PDF

---

*Built with ❤️ for interview preparation — because understanding beats memorizing.*
