# AppSec Foundry

Application security tools and research for teams using AI assistants to write and change code.

## [AppSec Advisor](https://github.com/appsec-foundry/appsec-advisor)

A Claude Code plugin that provides a couple of AppSec tool capabilities. Primarily, it derives a technical 
(implementation-level) threat model from code by using a sophisticated multi-agent pipeline.

## [AppSec Advisor Packaging Template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)

Package `appsec-advisor` as an internal plugin with your own requirements catalog, defaults and
cost guardrails, without maintaining a fork of the analysis pipeline.

## [AI Secure Coding Baseline (aiscb)](https://github.com/appsec-foundry/aiscb)

A compact, tool-neutral rule set for secure AI-assisted coding. Add it to a project's instructions so Claude Code, GitHub Copilot, Codex, and other compatible assistants apply it whenever they write or change code. At roughly 4,000 tokens, it is small enough to remain loaded throughout a session. `aiscb` is also bundled into the AppSec Advisor plugin.
