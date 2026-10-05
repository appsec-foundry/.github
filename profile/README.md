<h1 align="center">AppSec Foundry</h1>

<p align="center">
  <b>Open-source application security, mostly with an AI focus.</b><br>
  Threat modeling, secure code assistant, security reviews, and secure-coding guidance.
</p>

## 🛡️ appsec-advisor

[**appsec-advisor**](https://github.com/appsec-foundry/appsec-advisor) is a Claude Code plugin that builds STRIDE threat models from repository code and configuration. It also supports requirements audits, change reviews, and CI gates. *Currently in beta.*

<p align="center">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/advisor-attack-paths.png" alt="Excerpt from the OWASP Juice Shop threat model: attack paths from an anonymous attacker through the application and data tiers to business impact" width="100%">
</p>

<p align="center"><sub>Excerpt from the OWASP Juice Shop threat model: attack paths from an anonymous attacker to business impact.</sub></p>

### Try it

```bash
claude plugin marketplace add appsec-foundry/appsec-advisor
claude plugin install appsec-advisor@appsec-foundry
```

Then run `/appsec-advisor:create-threat-model` inside any repository.

### Companion repositories

| Repository | What it does |
|---|---|
| [**appsec-advisor-examples**](https://github.com/appsec-foundry/appsec-advisor-examples) | Example threat models for deliberately vulnerable apps such as OWASP Juice Shop, available as Markdown, HTML, PDF, YAML, SARIF, and Threat Dragon files. |
| [**appsec-advisor-tools**](https://github.com/appsec-foundry/appsec-advisor-tools) | Scripts for running appsec-advisor from a terminal, cron job, or CI pipeline, with repository profiling and templates for GitHub Actions and GitLab CI. |
| [**appsec-advisor-packaging-template**](https://github.com/appsec-foundry/appsec-advisor-packaging-template) | A template for packaging appsec-advisor as an internal Claude Code plugin with your organization's configuration. |

## 📏 aiscb: AI Secure Coding Baseline

[**aiscb**](https://github.com/appsec-foundry/aiscb) provides secure-coding rules for AI coding assistants such as Claude Code, GitHub Copilot, and Codex.

<p align="center">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/aiscb-security-choices.png" alt="Claude Code output for a generated Flask login app, listing the security choices shaped by the baseline" width="100%">
</p>

<p align="center"><sub>Excerpt from Claude Code output for a generated Flask login app: the security choices the baseline shaped.</sub></p>

## <img src="https://raw.githubusercontent.com/appsec-foundry/tss-web/main/assets/img/logo1.png" alt="" height="28"> TSS-WEB *(discontinued)*

[**tss-web**](https://github.com/appsec-foundry/tss-web) is an open security requirements framework covering technical and organizational controls for developing and operating web applications and services. The content is no longer maintained or further developed.

---

Questions and bug reports are welcome in each project's issue tracker.
