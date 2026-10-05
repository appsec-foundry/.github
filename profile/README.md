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

## Projects

<table>
  <tr>
    <td width="46%" valign="top">
      <a href="https://github.com/appsec-foundry/appsec-advisor"><img src="https://raw.githubusercontent.com/appsec-foundry/appsec-advisor/main/docs/images/heatmap.png" alt="Attack paths in OWASP Juice Shop, from threat actors through architecture tiers to business impact"></a>
    </td>
    <td valign="top">
      <h3><a href="https://github.com/appsec-foundry/appsec-advisor">appsec-advisor</a></h3>
      A Claude Code plugin that builds STRIDE threat models from repository code and configuration. It also supports requirements audits, change reviews, and CI gates. <i>Currently in beta.</i>
    </td>
  </tr>
  <tr>
    <td width="46%" valign="top">
      <a href="https://github.com/appsec-foundry/appsec-advisor-examples"><img src="https://raw.githubusercontent.com/appsec-foundry/appsec-advisor-examples/main/threat-modeler/threat-model-juice-shop-thorough-v0.6.0b4.figure1.svg" alt="Architecture overview figure from the OWASP Juice Shop threat model"></a>
    </td>
    <td valign="top">
      <h3><a href="https://github.com/appsec-foundry/appsec-advisor-examples">appsec-advisor-examples</a></h3>
      Example threat models produced by appsec-advisor for deliberately vulnerable apps such as OWASP Juice Shop, available as Markdown, HTML, PDF, YAML, SARIF, and Threat Dragon files.
    </td>
  </tr>
  <tr>
    <td width="46%" valign="top">
      <a href="https://github.com/appsec-foundry/aiscb"><img src="https://raw.githubusercontent.com/appsec-foundry/aiscb/main/docs/images/example_create_flask_with_aiscb_highlighted.png" alt="Claude Code output for a Flask login app, with the security choices and a security note shaped by the baseline highlighted"></a>
    </td>
    <td valign="top">
      <h3><a href="https://github.com/appsec-foundry/aiscb">aiscb</a></h3>
      The AI Secure Coding Baseline provides secure-coding rules for AI coding assistants such as Claude Code, GitHub Copilot, and Codex. The screenshot shows a generated Flask login app: the highlighted parts are choices the baseline shaped.
    </td>
  </tr>
  <tr>
    <td width="46%" valign="top">
      <a href="https://github.com/appsec-foundry/appsec-advisor-packaging-template"><img src="https://raw.githubusercontent.com/appsec-foundry/appsec-advisor/main/docs/images/orgpackaging.svg" alt="Rollout from an upstream appsec-advisor release to an organization-branded plugin"></a>
    </td>
    <td valign="top">
      <h3><a href="https://github.com/appsec-foundry/appsec-advisor-packaging-template">appsec-advisor-packaging-template</a></h3>
      A template for packaging appsec-advisor as an internal Claude Code plugin with your organization's configuration.
    </td>
  </tr>
  <tr>
    <td width="46%" valign="top">
      <a href="https://github.com/appsec-foundry/appsec-advisor-tools"><pre>./create-threat-model.sh \
  --target-dir ~/myapp

python3 repo_profile.py \
  --repo ~/myapp</pre></a>
    </td>
    <td valign="top">
      <h3><a href="https://github.com/appsec-foundry/appsec-advisor-tools">appsec-advisor-tools</a></h3>
      Companion scripts for running appsec-advisor threat modeling from a terminal, cron job, or CI pipeline, with repository profiling and templates for GitHub Actions and GitLab CI.
    </td>
  </tr>
</table>

### Discontinued

[**tss-web**](https://github.com/appsec-foundry/tss-web): an open security requirements framework covering technical and organizational controls for developing and operating web applications and services. The content is no longer maintained or further developed.

Questions and bug reports are welcome in each project's issue tracker.
