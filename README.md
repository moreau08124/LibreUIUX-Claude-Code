<p align="center">
  <img src="https://ormus.solutions/mascot/pixellab_liquid_to_swan.gif" alt="LibreUIUX Claude Code" width="128" style="image-rendering: pixelated;" />
</p>

<h1 align="center">LibreUIUX Claude Code</h1>

<p align="center">
  <em>Complete UI/UX system for Claude Code -- 71 plugins, 152 agents, 76 commands, 74 skills, 3 hooks</em>
</p>

<p align="center">
  <a href="https://github.com/HermeticOrmus/LibreUIUX-Claude-Code/stargazers"><img src="https://img.shields.io/github/stars/HermeticOrmus/LibreUIUX-Claude-Code?style=flat-square&color=aa8142" alt="Stars" /></a>
  <a href="https://github.com/HermeticOrmus/LibreUIUX-Claude-Code/blob/main/LICENSE"><img src="https://img.shields.io/github/license/HermeticOrmus/LibreUIUX-Claude-Code?style=flat-square&color=aa8142" alt="License" /></a>
  <a href="https://github.com/HermeticOrmus/LibreUIUX-Claude-Code/commits"><img src="https://img.shields.io/github/last-commit/HermeticOrmus/LibreUIUX-Claude-Code?style=flat-square&color=aa8142" alt="Last Commit" /></a>
  <img src="https://img.shields.io/badge/TypeScript-aa8142?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Claude Code-aa8142?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code" />
</p>

---
> **Skills, Agents, Commands, and Workflows for Modern UI/UX Development with Claude Code**

Stop getting the same outdated, Bootstrap-era designs. This repository provides a comprehensive, layered approach to dramatically improve the UI/UX components Claude Code generates for your projects.

---

## The New Programming Paradigm

In December 2025, Andrej Karpathy observed that programming is being "dramatically refactored":

> *"I've never felt this much behind as a programmer. The profession is being dramatically refactored."*
>
> *"New vocabulary: agents, subagents, their prompts, contexts, memory, modes, permissions, tools, plugins, skills, hooks, MCP, LSP, slash commands, workflows, IDE integrations..."*

He described Claude Code as *"the first convincing demonstration of what an LLM Agent looks like"* - a "little spirit/ghost that lives on your computer."

**LibreUIUX provides the skills, agents, commands, and workflows for this new paradigm - focused on UI/UX development.**

### Where LibreUIUX Fits

| New Stack Component | LibreUIUX Provides |
|---------------------|-------------------|
| **Skills** | 74 specialized skills (accessibility, animation, design systems, etc.) |
| **Agents** | 152 agent definitions across the plugins (93 distinct agents; shared ones such as `code-reviewer` ship in several plugins) |
| **Commands** | 76 slash commands across the plugins (65 distinct) |
| **Plugins** | 71 installable plugins (frontend, accessibility, design mastery, etc.) |
| **Hooks** | 3 optional hooks in `libreuiux-hooks` (stack context, secrets-file confirmation, accessibility hints) |
| **Workflows** | Beginner to advanced learning paths |

This isn't just a prompt library. It's infrastructure for the new way we build software with AI.

---

## What's Included

```
LibreUIUX-Claude-Code/
├── 71 Plugins         # Installable from the libreuiux marketplace
├── 152 Agents         # Task-specialized AI personas (93 distinct)
├── 76 Commands        # Slash commands for Claude Code (65 distinct)
├── 74 Skills          # Reusable capability modules
├── 3 Hooks            # Optional, in the libreuiux-hooks plugin
├── 3 Skill Levels     # Beginner → Intermediate → Advanced
└── Templates          # Ready-to-use configurations
```

### Plugin Categories

| Category | Plugins | Description |
|----------|---------|-------------|
| **Frontend & UI** | design-mastery, frontend-mobile-development, accessibility-compliance | Core UI/UX development |
| **Backend Integration** | backend-development, api-scaffolding, database-design | Full-stack patterns |
| **Quality & Testing** | unit-testing, tdd-workflows, code-review-ai | Ensure production quality |
| **DevOps & Deploy** | cicd-automation, deployment-strategies, kubernetes-operations | Ship with confidence |
| **Specialized** | game-development, blockchain-web3, machine-learning-ops | Domain expertise |

### Skills vs Commands vs Agents

| Component | When to Use | Example |
|-----------|-------------|---------|
| **Skills** | Need domain knowledge applied to a task | `api-design-principles` - teaches REST best practices |
| **Commands** | Quick, repeatable actions | `/ui-critique` - get instant design feedback |
| **Agents** | Complex, multi-step work requiring expertise | `frontend-developer` - builds complete components |

---

## Quick Start

### Install from Claude Code

```
/plugin marketplace add HermeticOrmus/LibreUIUX-Claude-Code
/plugin install design-mastery@libreuiux
```

Install any other plugin the same way (`/plugin install accessibility-compliance@libreuiux`), or browse them all with `/plugin`. The same thing from a terminal:

```bash
claude plugin marketplace add HermeticOrmus/LibreUIUX-Claude-Code
claude plugin install design-mastery@libreuiux
```

From a clone, `./setup.sh` installs every plugin through the Claude Code CLI (`./setup.sh --list` to see them, `--only design-mastery,accessibility-compliance` for a subset, `--scope project` for one project, `--uninstall` to remove them). The optional hooks are one more plugin: `/plugin install libreuiux-hooks@libreuiux`. Restart Claude Code after installing.

To drop a LibreUIUX `CLAUDE.md` template and config into a project instead, run `./bootstrap.sh` from inside that project (this was `setup.sh` before 2.0.0).

### Install in Grok Build

Grok Build loads the same plugin folders. Add the marketplace and install a plugin from a terminal:

```bash
grok plugin marketplace add HermeticOrmus/LibreUIUX-Claude-Code
grok plugin install design-mastery@LibreUIUX-Claude-Code
```

Or install one plugin straight from its folder, with no marketplace:

```bash
grok plugin install HermeticOrmus/LibreUIUX-Claude-Code#plugins/design-mastery
```

From a clone, `./setup.sh --grok` installs every plugin through the `grok` CLI; `--only`, `--list`, and `--uninstall` work the same way. Grok Build uninstalls plugins by name only, and 66 plugin names here are also in [claude-code-game-development](https://github.com/HermeticOrmus/claude-code-game-development) (both packs take them from wshobson/agents), as is `design-mastery` in [design-mastery-claude-code](https://github.com/HermeticOrmus/design-mastery-claude-code). If you install more than one of these packs, remove one with `./setup.sh --grok --uninstall` rather than `grok plugin uninstall <name>`, which can take the other pack's copy. The `libreuiux-hooks` plugin uses a hook format Grok Build supports, but it has not been verified in a live Grok session yet.

### Migrating from 1.x

Version 2.0.0 renames the marketplace from `claude-code-workflows` to `libreuiux`. The old name is also the name of [wshobson/agents](https://github.com/wshobson/agents), so anyone with that marketplace installed could not add this one. The plugins keep their names.

1. Run `/plugin marketplace list` (or `claude plugin marketplace list` in a terminal) and check which repository `claude-code-workflows` points to.
2. Only if it points to `HermeticOrmus/LibreUIUX-Claude-Code`, remove it: `/plugin marketplace remove claude-code-workflows`. If it points to `wshobson/agents`, leave it alone.
3. Add this repository again: `/plugin marketplace add HermeticOrmus/LibreUIUX-Claude-Code`, then reinstall what you use as `<plugin>@libreuiux`.

Prefer the dedicated walkthrough: **[QUICK_START.md](./QUICK_START.md)** (about 5 minutes).

### Installation Paths

**Path 1: Drop-in CLAUDE.md** (fastest — recommended)
```bash
cd your-project
curl -fsSL https://raw.githubusercontent.com/HermeticOrmus/LibreUIUX-Claude-Code/main/templates/CLAUDE.modern-webapp.md -o CLAUDE.md
claude
```

**Path 2: Just want better prompts?** (5 minutes)
```bash
# Browse beginner prompts after cloning
git clone --depth 1 https://github.com/HermeticOrmus/LibreUIUX-Claude-Code.git
cat LibreUIUX-Claude-Code/beginner/prompts/modern-button.md
```

**Path 3: Add commands to Claude Code** (10 minutes)
```bash
cp -r .claude/commands/* ~/.claude/commands/
```

**Path 4: Use a specific plugin** (15 minutes)
```bash
# Example: design mastery
mkdir -p your-project/.claude/agents your-project/.claude/skills
cp plugins/design-mastery/agents/* your-project/.claude/agents/
# copy individual skill folders as needed from plugins/design-mastery/skills/
```

**Path 5: Full installation**
```bash
git clone https://github.com/HermeticOrmus/LibreUIUX-Claude-Code.git
cd LibreUIUX-Claude-Code
# see QUICK_START.md and beginner/README.md
```

Contributions: see **[CONTRIBUTING.md](./CONTRIBUTING.md)**. License: **[MIT](./LICENSE)**.

---

## The Problem

Developers using Claude Code face these challenges:

- **Repetitive Designs**: Claude generates similar-looking components regardless of project context
- **Outdated Aesthetics**: Components resemble old Bootstrap-era designs (2015-2018)
- **Poor Responsiveness**: Generated layouts don't adapt well to different screen sizes
- **Generic Feel**: Lack of modern design patterns, animations, and interactions
- **Inconsistent Results**: Same prompts produce varying quality across sessions

### Real Developer Experiences

> *"No matter what I try, the UI components generated with Claude Code look outdated. They often resemble older Bootstrap-era designs and are not responsive."*

> *"I've tried custom commands, design agents, detailed prompting, even Claude Opus... nothing consistently works."*

**The core issue**: Claude Code needs specific, structured guidance to generate modern UI/UX.

---

📝 **Field Notes from the Trenches**

I spent two weeks fighting this. "Make it modern." "Use better colors." "Improve the spacing." Every request felt like rolling dice.

Then I tried: "Create a button with bg-blue-600, hover:bg-blue-700, px-6 py-3, rounded-lg, shadow-md."

Perfect. First try. Every time.

**Here's what clicked:** Claude understands design systems perfectly—Tailwind's scale, spacing units, color tokens. When you speak that precise language instead of vague aesthetics, you're giving coordinates instead of directions.

**Try this:** Compare "make it look better" vs "change shadow-md to shadow-lg and p-4 to p-6"

**Watch for:** The second request gives you exactly what you want, immediately.

**This works because:** You're leveraging Claude's systematic understanding instead of fighting it. That's what this entire repository teaches—the elegant mechanics of communicating design intent precisely.

---

## 🎨 The Solution: Layered Approach

Here's what's beautiful about this repository's approach: instead of one-size-fits-all advice, we've built a **progressive learning system**. Start where you are, grow as you need.

This repository provides solutions for **all skill levels**:

### 🟢 Beginner Level
**Goal**: Get better results immediately with minimal setup

- **Ready-to-use prompts** for modern UI components
- **Component request templates** with proper specificity
- **Design vocabulary guide** - speak the language of modern UI/UX
- **Quick-start checklist** for every UI task

👉 [Start Here: Beginner Guide](./beginner/README.md)

### 🟡 Intermediate Level
**Goal**: Build systematic workflows for consistent results

- **Design system templates** (color schemes, typography, spacing)
- **Custom CLAUDE.md configurations** for your projects
- **Component library integrations** (Shadcn, Aceternity, etc.)
- **Iteration workflows** using browser tools
- **Before/After examples** with detailed breakdowns

👉 [Level Up: Intermediate Techniques](./intermediate/README.md)

### 🔴 Advanced/Pro Level
**Goal**: Create a powerful, automated UI/UX development environment

- **MCP Server setups** (Chrome DevTools integration)
- **Custom slash commands** for Claude Code
- **Automated design systems**
- **AI-assisted design critique workflows**
- **Production-ready component architectures**

👉 [Master Level: Advanced Solutions](./advanced/README.md)

---

## Repository Structure

```
LibreUIUX-Claude-Code/
├── README.md                          # You are here
│
├── plugins/                           # 71 installable plugins
│   ├── design-mastery/               # UI/UX design expertise
│   │   ├── agents/                   # Specialized AI agents
│   │   ├── commands/                 # Slash commands
│   │   └── skills/                   # Reusable skill modules
│   ├── accessibility-compliance/     # WCAG, ARIA, a11y testing
│   ├── frontend-mobile-development/  # React, Vue, React Native, etc.
│   ├── backend-development/          # APIs, databases, architecture
│   ├── cicd-automation/              # Deployment, pipelines, DevOps
│   ├── libreuiux-hooks/              # Optional hooks (session context, secrets, a11y hints)
│   └── ... (65 more plugins)         # See full list below
│
├── beginner/                          # Start here if new
│   ├── README.md                      # Beginner guide overview
│   ├── design-vocabulary.md           # Learn the language of modern UI
│   ├── prompts/                       # Ready-to-use prompt templates (button, card, form, nav)
│   └── checklist.md                   # Pre-request checklist
│
├── intermediate/                      # Build systematic workflows
│   ├── README.md                      # Intermediate guide overview
│   ├── design-systems/                # Design system template (modern web app)
│   └── workflows/                     # Iteration workflow
│
├── advanced/                          # Pro-level automation
│   └── README.md                      # Advanced guide overview
│
├── resources/                         # Curated resources
│   ├── component-libraries.md         # Library comparisons & links
│   ├── tools.md                       # Recommended tools
│   └── github-repos.md                # Curated GitHub repositories
│
├── templates/                         # Copy-paste CLAUDE.md templates
│   ├── CLAUDE.md                      # Template for project root
│   ├── CLAUDE.minimal.md
│   ├── CLAUDE.mobile-first.md
│   ├── CLAUDE.modern-webapp.md
│   └── CLAUDE.saas-platform.md
│
├── hooks/                             # Original hook scripts (use the libreuiux-hooks plugin)
├── demo/                              # Demo page and checklist
├── setup.sh                           # Install the plugins through the Claude Code CLI
├── bootstrap.sh                       # Add a CLAUDE.md template and config to a project
├── NOTICE.md                          # Credit and license for the wshobson/agents plugins
├── pantry/                            # Research and the Menu of open work (pantry/MENU.md)
│
└── .claude/                           # Claude Code configuration for this repo
    ├── agents/
    │   └── synthesis-master.md
    └── commands/                      # Slash commands (copy to ~/.claude/commands to use elsewhere)
        ├── ui-modern.md
        ├── ui-critique.md
        ├── ui-responsive.md
        ├── ui-review.md
        └── ui-synth.md
```

### All 71 Plugins

<details>
<summary>Click to expand full plugin list</summary>

| Plugin | Focus Area |
|--------|------------|
| accessibility-compliance | WCAG, ARIA, screen readers |
| agent-orchestration | Multi-agent coordination |
| api-scaffolding | REST/GraphQL API design |
| api-testing-observability | API testing & monitoring |
| application-performance | Frontend/backend optimization |
| archetypal-alchemy \* | Design psychology patterns |
| arm-cortex-microcontrollers | Embedded systems |
| backend-api-security | Auth, validation, security |
| backend-development | Server architecture |
| blockchain-web3 | Smart contracts, DeFi |
| business-analytics | Data analysis, reporting |
| cicd-automation | CI/CD pipelines |
| cloud-infrastructure | AWS, GCP, Azure |
| codebase-cleanup | Refactoring, debt reduction |
| code-documentation | Docs generation |
| code-refactoring | Pattern improvement |
| code-review-ai | Automated review |
| comprehensive-review | Full codebase audits |
| content-marketing | SEO, content strategy |
| context-management | Claude context optimization |
| customer-sales-automation | CRM, automation |
| database-cloud-optimization | DB performance |
| database-design | Schema, modeling |
| database-migrations | Safe migrations |
| data-engineering | ETL, pipelines |
| data-validation-suite | Input validation |
| debugging-toolkit | Debug strategies |
| dependency-management | Package management |
| deployment-strategies | Blue-green, canary |
| deployment-validation | Deploy verification |
| design-mastery \* | UI/UX excellence |
| developer-essentials | Core dev workflows |
| distributed-debugging | Microservice debugging |
| documentation-generation | Auto-docs |
| error-debugging | Error analysis |
| error-diagnostics | Root cause analysis |
| framework-migration | Version upgrades |
| frontend-mobile-development | React, Vue, mobile |
| frontend-mobile-security | XSS, CSRF protection |
| full-stack-orchestration | End-to-end coordination |
| functional-programming | FP patterns |
| game-development | Game engines, graphics |
| git-pr-workflows | Git best practices |
| hr-legal-compliance | Privacy, GDPR |
| incident-response | Outage handling |
| javascript-typescript | JS/TS patterns |
| julia-development | Julia lang |
| jvm-languages | Java, Kotlin, Scala |
| kubernetes-operations | K8s management |
| libreuiux-hooks \* | Optional hooks: stack context, secrets-file confirmation, accessibility hints |
| llm-application-dev | AI/LLM apps |
| machine-learning-ops | MLOps |
| mcp-integrations \* | MCP server tools & browser DevTools |
| multi-platform-apps | Cross-platform |
| observability-monitoring | Logging, metrics |
| payment-processing | Stripe, payments |
| performance-testing-review | Load testing |
| python-development | Python patterns |
| quantitative-trading | Algo trading |
| security-compliance | Security audits |
| security-scanning | Vuln detection |
| seo-analysis-monitoring | SEO tracking |
| seo-content-creation | SEO writing |
| seo-technical-optimization | Technical SEO |
| shell-scripting | Bash, automation |
| systems-programming | Low-level dev |
| tdd-workflows | Test-driven dev |
| team-collaboration | Team processes |
| unit-testing | Testing strategies |
| vibe-coding \* | Rapid AI-assisted prototyping |
| web-scripting | Scraping, automation |

\* Original to LibreUIUX. The other 66 plugins derive from [wshobson/agents](https://github.com/wshobson/agents) by Seth Hobson (MIT); see [NOTICE.md](./NOTICE.md).

</details>

---

## 🎓 Learning Path

### Week 1: Fundamentals
1. Read [Design Vocabulary](./beginner/design-vocabulary.md)
2. Try 3 component prompts from [beginner/prompts/](./beginner/prompts/)
3. Practice with the prompts to see before/after transformations

### Week 2: Systems Thinking
1. Choose a [design system template](./intermediate/design-systems/)
2. Create a CLAUDE.md file for your project
3. Practice the [iteration workflow](./intermediate/workflows/iteration-workflow.md)

### Week 3+: Advanced Techniques
1. Set up [Chrome DevTools MCP](./advanced/mcp-servers/chrome-devtools/)
2. Install [custom slash commands](./advanced/slash-commands/)
3. Build your own component library

---

## 🔑 Key Principles

Think of these as the elegant mechanics of communicating with Claude. Each principle solves a specific problem in how AI interprets design intent.

### ✅ Do This
- **Be specific**: "glassmorphism card with backdrop-blur-md, subtle border, 12px padding"
  - *Why it works:* Precision eliminates ambiguity. Claude executes specifications, not aesthetics.

- **Reference examples**: "Like the pricing card on https://ui.shadcn.com"
  - *Why it works:* Concrete references create shared understanding instantly.

- **Use design systems**: Define colors, spacing, typography upfront
  - 