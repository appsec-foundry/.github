# AppSec Foundry

Application security tools and research, aimed at what happens when AI assistants write the code.

Assistants know a lot of security practice and apply it unevenly. They also reshape an
architecture faster than a threat model kept in a document survives. The projects here work on
both ends of that: rules that go into the assistant's instructions, and analysis that reads the
repository afterwards.

## [appsec-advisor](https://github.com/appsec-foundry/appsec-advisor)

A Claude Code plugin that derives a threat model from code. It reconstructs components, data flows
and trust boundaries from the repository, runs STRIDE against that model, and points at the
evidence behind every finding. Run it again once the code has moved and the model follows.

Where SAST asks whether an implementation is vulnerable, this asks whether the design leans on
controls the implementation never had. It also handles requirements audits, change reviews and CI
gates.

## [ai-secure-coding-baseline](https://github.com/appsec-foundry/ai-secure-coding-baseline)

A short rule set you drop into a project's instructions so Claude Code, Copilot, Codex and the
others apply it while writing and changing code. Roughly 4,000 tokens, small enough to keep loaded
permanently. `appsec-advisor` installs it with `/appsec-advisor:install-baseline`.

## [appsec-advisor-packaging-template](https://github.com/appsec-foundry/appsec-advisor-packaging-template)

Package `appsec-advisor` as an internal plugin with your own requirements catalog, defaults and
cost guardrails, without maintaining a fork of the analysis pipeline.

## Status

Everything here is beta and can change without notice. The analysis sees only what is in the
repository, so runtime behaviour, production-only controls and business processes stay out of
reach; someone should check the findings before they turn into remediation work or a risk
acceptance. Scanned repositories are untrusted input and may carry prompt injection, so keep
third-party code in a container or VM.
