Open-source application security projects, mostly with an AI focus: appsec-advisor for threat modeling, aiscb for secure coding with AI assistants, and the discontinued TSS-WEB requirements framework.

## appsec-advisor

[![Latest release](https://img.shields.io/github/v/release/appsec-foundry/appsec-advisor)](https://github.com/appsec-foundry/appsec-advisor/releases/latest)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-advisor/blob/main/LICENSE)
[![Claude Code plugin](https://img.shields.io/badge/Claude%20Code-plugin-5A67D8)](https://github.com/appsec-foundry/appsec-advisor)

[**appsec-advisor**](https://github.com/appsec-foundry/appsec-advisor) is a Claude Code plugin that derives a threat model from the implementation in a code repository.

- Reconstructs components, data flows, and trust boundaries from code and configuration.
- Identifies threats and control gaps. Every finding points to evidence in the repository and comes with remediation guidance.
- Also assesses planned features and single code changes, audits requirements, and runs as a CI gate.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/advisor-figure1-v3-dark.png">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/advisor-figure1-v3.png" alt="Excerpt from Figure 1a of the OWASP Juice Shop threat model: internet attacker and users, trust boundaries, and the authentication component with its findings and assets" width="100%">
</picture>

<sub>Excerpt from Figure 1a of the OWASP Juice Shop threat model: the architecture derived from the repository, with findings per component and the assets each layer stores.</sub>

```bash
claude plugin marketplace add appsec-foundry/appsec-advisor
claude plugin install appsec-advisor@appsec-foundry
```

Then run `/appsec-advisor:create-threat-model` inside any repository.

| Companion repository | What it does |
|---|---|
| [**appsec-advisor-examples**](https://github.com/appsec-foundry/appsec-advisor-examples) | Example threat models for deliberately vulnerable apps such as OWASP Juice Shop, available as Markdown, HTML, PDF, YAML, SARIF, and Threat Dragon files. |
| [**appsec-advisor-tools**](https://github.com/appsec-foundry/appsec-advisor-tools) | Scripts for running appsec-advisor from a terminal, cron job, or CI pipeline, with repository profiling and templates for GitHub Actions and GitLab CI. |
| [**appsec-advisor-packaging-template**](https://github.com/appsec-foundry/appsec-advisor-packaging-template) | A template for packaging appsec-advisor as an internal Claude Code plugin with your organization's configuration. |

## aiscb: AI Secure Coding Baseline

[![Latest release](https://img.shields.io/github/v/release/appsec-foundry/aiscb)](https://github.com/appsec-foundry/aiscb/releases/latest)
[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](https://github.com/appsec-foundry/aiscb/blob/main/LICENSE)

[**aiscb**](https://github.com/appsec-foundry/aiscb) provides secure-coding rules for AI coding assistants.

**Supported assistants:** Claude Code · GitHub Copilot · OpenAI Codex · Kiro

- A compact core stays in the assistant's context on every prompt.
- Topic modules such as web authentication, secrets, or supply chain load only when a task needs them.
- The assistant applies the rules while it writes code and reports remaining risks in a security note.

<img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/aiscb-crypto-with-without.png" alt="The same prompt in Claude Code without and with aiscb: without it, Claude writes a custom cipher; with it, Claude cites the baseline rule against hand-rolled crypto and asks what the code is for" width="100%">

<sub>The same prompt in Claude Code, without and with aiscb. Without the baseline, Claude writes a custom cipher. With it, Claude cites the rule against hand-rolled crypto and asks what the code is for.</sub>

## <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/tss-web-logo.png" alt="" height="28"> TSS-WEB

[![Status: discontinued](https://img.shields.io/badge/status-discontinued-lightgrey)](https://github.com/appsec-foundry/tss-web)
[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](https://github.com/appsec-foundry/tss-web/blob/main/LICENSE)

[**tss-web**](https://github.com/appsec-foundry/tss-web) is an open security requirements framework for web applications and services.

- Covers technical and organizational controls for developing and operating web applications.
- Sits between high-level security policies such as ISO/IEC 27001 and technology-specific secure-coding guidelines.
- No longer maintained or further developed.

---

Questions and bug reports are welcome in each project's issue tracker.

**Maintainer:** Matthias Rohr &nbsp;<a href="https://www.linkedin.com/in/matthias-rohr/"><img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/linkedin.png" alt="LinkedIn" height="16" align="absmiddle"></a> [LinkedIn](https://www.linkedin.com/in/matthias-rohr/)
