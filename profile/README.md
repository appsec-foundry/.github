<div align="center">

# AppSec Foundry

**Application security tools and research for teams using AI assistants to write and change code.**

</div>

## Projects

AppSec Advisor is the place to start; the baseline also works on its own.

- **[AppSec Advisor](https://github.com/appsec-foundry/appsec-advisor)** — derives a technical, implementation-level threat model from a repository through a multi-agent pipeline, runs STRIDE against it, and cites the code evidence behind every finding. Also covers requirements audits, change reviews, and CI gates.<br><sub>Claude Code plugin · Apache-2.0 · [Quick start →](https://github.com/appsec-foundry/appsec-advisor#quick-start)</sub>

- **[AI Secure Coding Baseline](https://github.com/appsec-foundry/aiscb)** — a compact, tool-neutral secure-coding rule set for a project's instructions, applied by Claude Code, GitHub Copilot, Codex, and other compatible assistants. At roughly 4,000 tokens it stays loaded for a whole session. Bundled with AppSec Advisor.<br><sub>`aiscb` · CC BY 4.0 · [Quick start →](https://github.com/appsec-foundry/aiscb#quick-start)</sub>

- **[Packaging Template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)** — ships AppSec Advisor as an internal plugin with your own requirements catalog, defaults, and cost guardrails, without maintaining a fork of the analysis pipeline.<br><sub>Apache-2.0 · [Quick start →](https://github.com/appsec-foundry/appsec-advisor-packaging-template#quick-start)</sub>

---

<div align="center">
<sub>Beta — interfaces and output can change without notice. Findings need review before they drive remediation or risk acceptance.<br>Questions, bugs, and ideas belong in the issue tracker of the project they concern.</sub>
</div>
