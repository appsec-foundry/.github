# AppSec Foundry

Application security tools and research, aimed at what happens when AI assistants write the code.

## [appsec-advisor](https://github.com/appsec-foundry/appsec-advisor)

A Claude Code plugin that derives a threat model from code and provider other appsec skills.
It reconstructs components, data flows and trust boundaries from the repository, runs STRIDE against that model, 
and points at the evidence behind every finding. Run it again once the code has moved and the model follows.

## [appsec-advisor-packaging-template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)

Package `appsec-advisor` as an internal plugin with your own requirements catalog, defaults and
cost guardrails, without maintaining a fork of the analysis pipeline.

## [AI Secure Coding Baseline (aiscb)](https://github.com/appsec-foundry/aiscb)

A compact, tool-neutral rule set for secure AI-assisted coding. Add it to a project's instructions so Claude Code, GitHub Copilot, Codex, and other compatible assistants apply it whenever they write or change code. At roughly 4,000 tokens, it is small enough to remain loaded throughout a session.

Install it with appsec-advisor using `/appsec-advisor:install-baseline`.
