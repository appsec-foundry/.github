# AppSec Foundry

Application security tools and research, aimed at what happens when AI assistants write the code.

## [appsec-advisor](https://github.com/appsec-foundry/appsec-advisor)

A Claude Code plugin that derives a threat model from code and provider other appsec skills.
It reconstructs components, data flows and trust boundaries from the repository, runs STRIDE against that model, 
and points at the evidence behind every finding. Run it again once the code has moved and the model follows.

## [appsec-advisor-packaging-template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)

Package `appsec-advisor` as an internal plugin with your own requirements catalog, defaults and
cost guardrails, without maintaining a fork of the analysis pipeline.

## [ai-secure-coding-baseline](https://github.com/appsec-foundry/ai-secure-coding-baseline)

A short rule set you drop into a project's instructions so Claude Code, Copilot, Codex and the
others apply it while writing and changing code. Roughly 4,000 tokens, small enough to keep loaded
permanently. `appsec-advisor` installs it with `/appsec-advisor:install-baseline`.
