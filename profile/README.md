<h1 align="center">AppSec Foundry</h1>

<p align="center">
  <b>Open-source application security, mostly with an AI focus.</b><br>
  Threat modeling, secure code assistant, security reviews, and secure-coding guidance.
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/appsec-foundry/appsec-advisor/main/docs/images/threat-model-pipeline.png" alt="appsec-advisor pipeline: understand the repository, think about threats, prioritize and report, quality loop" width="100%">
</p>

<p align="center"><sub>The appsec-advisor pipeline: from a code repository to a threat model with prioritized findings.</sub></p>

## Try it in two commands

```bash
claude plugin marketplace add appsec-foundry/appsec-advisor
claude plugin install appsec-advisor@appsec-foundry
```

Then run `/appsec-advisor:create-threat-model` inside any repository.

## Threat modeling

| Project | What it does |
|---|---|
| [**appsec-advisor**](https://github.com/appsec-foundry/appsec-advisor) | A Claude Code plugin that builds STRIDE threat models from repository code and configuration. It also supports requirements audits, change reviews, and CI gates. *Currently in beta.* |
| [**appsec-advisor-examples**](https://github.com/appsec-foundry/appsec-advisor-examples) | Example threat models for deliberately vulnerable apps such as OWASP Juice Shop, available as Markdown, HTML, PDF, YAML, SARIF, and Threat Dragon files. |
| [**appsec-advisor-tools**](https://github.com/appsec-foundry/appsec-advisor-tools) | Companion scripts for running appsec-advisor from a terminal, cron job, or CI pipeline, with repository profiling and templates for GitHub Actions and GitLab CI. |
| [**appsec-advisor-packaging-template**](https://github.com/appsec-foundry/appsec-advisor-packaging-template) | A template for packaging appsec-advisor as an internal Claude Code plugin with your organization's configuration. |

## Secure coding

| Project | What it does |
|---|---|
| [**aiscb**](https://github.com/appsec-foundry/aiscb) | The AI Secure Coding Baseline provides secure-coding rules for AI coding assistants such as Claude Code, GitHub Copilot, and Codex. |

## Discontinued

| Project | What it was |
|---|---|
| [**tss-web**](https://github.com/appsec-foundry/tss-web) | An open security requirements framework covering technical and organizational controls for developing and operating web applications and services. No longer maintained or further developed. |

Questions and bug reports are welcome in each project's issue tracker.
