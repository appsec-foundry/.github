<div align="center">

# AppSec Foundry

**Application security tools and research for teams using AI assistants to write and change code.**

[![Claude Code](https://img.shields.io/badge/Claude%20Code-plugins%20%26%20rules-D97757?logo=anthropic&logoColor=white)](https://code.claude.com/)
[![Threat modeling](https://img.shields.io/badge/threat%20modeling-code--derived-5A67D8)](https://github.com/appsec-foundry/appsec-advisor)
[![Status](https://img.shields.io/badge/status-beta-orange)](#)

</div>

---

## Projects

| Project | What it does | |
|---|---|---|
| **[AppSec Advisor](https://github.com/appsec-foundry/appsec-advisor)**<br><sub>Claude Code plugin · Apache-2.0</sub> | Derives a technical, implementation-level threat model from a repository through a multi-agent pipeline, runs STRIDE against it, and cites the code evidence behind every finding. Also covers requirements audits, change reviews, and CI gates. | [Quick start →](https://github.com/appsec-foundry/appsec-advisor#quick-start) |
| **[AI Secure Coding Baseline](https://github.com/appsec-foundry/aiscb)**<br><sub>`aiscb` · CC BY 4.0</sub> | A compact, tool-neutral secure-coding rule set for a project's instructions, applied by Claude Code, GitHub Copilot, Codex, and other compatible assistants. At roughly 4,000 tokens it stays loaded for a whole session. Bundled with AppSec Advisor. | [Quick start →](https://github.com/appsec-foundry/aiscb#quick-start) |
| **[Packaging Template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)**<br><sub>Apache-2.0</sub> | Ships AppSec Advisor as an internal plugin with your own requirements catalog, defaults, and cost guardrails — without maintaining a fork of the analysis pipeline. | [Quick start →](https://github.com/appsec-foundry/appsec-advisor-packaging-template#quick-start) |

---

<div align="center">
<sub>Beta — interfaces and output can change without notice. Findings need review before they drive remediation or risk acceptance.<br>Questions, bugs, and ideas belong in the issue tracker of the project they concern.</sub>
</div>
