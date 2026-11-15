Open-source application security projects, mostly with an AI focus.

## AppSec Analyzer

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-analyzer/blob/main/LICENSE)

[**appsec-analyzer**](https://github.com/appsec-foundry/appsec-analyzer) is a command-line tool for threat assessments of local and remote repositories. A deterministic controller runs the assessment and integrates the LLM: Claude by default, Codex and other providers experimentally.

- Combines deterministic scanners, a STRIDE-based threat survey, a catalog-based verifier, and abuse case checks. You can add your own abuse cases.
- Writes a Markdown report and a YAML data file, and exports to PDF, HTML, and other formats.
- Opens the findings in Claude Code or Codex for further analysis.

<a href="https://github.com/appsec-foundry/appsec-analyzer-examples">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/advisor-figure1-v3-dark.png">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/advisor-figure1-v3.png" alt="Excerpt from the architecture diagram of an OWASP Juice Shop assessment: internet attacker and users, trust boundaries, and the authentication component with its findings and assets" width="100%">
</picture>
</a>

<sub>Excerpt from an OWASP Juice Shop assessment, created with appsec-advisor: the architecture derived from the repository, with findings per component and the assets each layer stores.</sub>

[**appsec-analyzer-examples**](https://github.com/appsec-foundry/appsec-analyzer-examples) has example reports for OWASP Juice Shop and DVWA as Markdown and YAML files, with all diagrams as SVG.

## AppSec Verifier

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-verifier/blob/main/LICENSE)

[**appsec-verifier**](https://github.com/appsec-foundry/appsec-verifier) is a command-line tool that tests whether the findings of an appsec-analyzer assessment hold up in a running application you are authorized to test. It uses Claude by default, Codex and GitHub Copilot as alternatives.

- An AI agent plans the tests, but only a check in code confirms a finding, never the model's verdict alone.
- Tests cross-site scripting, access control, injection, path traversal, open redirect, and SSRF. Every request stays within the scope you define.
- Shows the requests behind each verdict, with evidence images and a HAR file.

<a href="https://github.com/appsec-foundry/appsec-verifier/blob/main/examples/juice-shop/result/verification.md#t-004">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/verifier-evidence-sqli-dark.png">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/verifier-evidence-sqli.png" alt="Evidence image of a SQL injection in OWASP Juice Shop: q=apple' gets status 500 with an SQLITE_ERROR, q=apple'' gets 200 with an empty result" width="100%">
</picture>
</a>

<sub>Evidence image from a run against OWASP Juice Shop. A single quote in the search parameter `q` causes a database error and two quotes do not, so the Verifier confirms the SQL injection.</sub>

The [Juice Shop example](https://github.com/appsec-foundry/appsec-verifier/tree/main/examples/juice-shop) has the complete run with console log, report, and all evidence images.

## AppSec Tools

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-tools/blob/main/LICENSE)

[**appsec-tools**](https://github.com/appsec-foundry/appsec-tools) has standalone tools that run deterministically, without an LLM.

- [**Security Score**](https://github.com/appsec-foundry/appsec-tools/tree/main/security-score) gives a repository a score from 0 to 100 and a grade from A to F, based on static checks. For a change, it rates the security relevance instead.

  <a href="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/security-score-details.png">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/security-score-details-crop-dark.png">
    <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/security-score-details-crop.png" alt="Excerpt of security-score --details on Juice Shop: repository overview, then the score and findings for the Repository and Authentication topics" width="100%">
  </picture>
  </a>

  <sub>Excerpt of `security-score --details` on OWASP Juice Shop, which is insecure on purpose. "partial" means that some topics could not be assessed, so there is no grade.</sub>

- [**Requirement Harvester**](https://github.com/appsec-foundry/appsec-tools/tree/main/requirement-harvester) reads requirements from websites and wikis and writes them to an OSCAL catalog in YAML.

## AppSec Skills

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-skills/blob/main/LICENSE)

[**appsec-skills**](https://github.com/appsec-foundry/appsec-skills) is a collection of application security skills for coding assistants, including:

- [**create-threat-model**](https://github.com/appsec-foundry/appsec-skills/blob/main/skills/create-threat-model/README.md) creates, updates, or reviews a threat model from requirements, design documents, and team knowledge, even before code exists.
- [**analyze-threats**](https://github.com/appsec-foundry/appsec-skills/blob/main/skills/analyze-threats/README.md) examines features, changes, pull requests, or design decisions for threats.

## aiscb: AI Secure Coding Baseline

[![Latest release](https://img.shields.io/github/v/release/appsec-foundry/aiscb)](https://github.com/appsec-foundry/aiscb/releases/latest)
[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](https://github.com/appsec-foundry/aiscb/blob/main/LICENSE)

[**aiscb**](https://github.com/appsec-foundry/aiscb) is a set of secure-coding rules for Claude Code, GitHub Copilot, OpenAI Codex, and Kiro.

- A compact core stays in the assistant's context on every prompt.
- Topic modules such as web, authentication, secrets, or supply chain load only when a task needs them.
- The assistant applies the rules while it writes code and reports remaining risks in a security note.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/aiscb-crypto-with-without-dark.png">
  <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/aiscb-crypto-with-without.png" alt="The same prompt in Claude Code without and with aiscb: without it, Claude writes a custom cipher; with it, Claude cites the baseline rule against hand-rolled crypto and asks what the code is for" width="100%">
</picture>

<sub>The same prompt in Claude Code, without and with aiscb. Without the baseline, Claude writes a custom cipher. With it, Claude cites the rule against hand-rolled crypto and asks what the code is for.</sub>

## AppSec Advisor

[![Status: being rebuilt](https://img.shields.io/badge/status-being%20rebuilt-orange)](https://github.com/appsec-foundry/appsec-advisor)
[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/appsec-foundry/appsec-advisor/blob/main/LICENSE)
[![Claude Code plugin](https://img.shields.io/badge/Claude%20Code-plugin-5A67D8)](https://github.com/appsec-foundry/appsec-advisor)

[**appsec-advisor**](https://github.com/appsec-foundry/appsec-advisor) is a Claude Code plugin for application security. Most of it has moved into [appsec-analyzer](https://github.com/appsec-foundry/appsec-analyzer), and the plugin is being rebuilt.

- [**appsec-advisor-examples**](https://github.com/appsec-foundry/appsec-advisor-examples) has example threat models for OWASP Juice Shop and other deliberately vulnerable apps.
- [**appsec-advisor-packaging-template**](https://github.com/appsec-foundry/appsec-advisor-packaging-template) is a template for packaging appsec-advisor as an internal plugin with your organization's configuration.

## <img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/tss-web-logo.png" alt="" height="28"> TSS-WEB

[![Status: discontinued](https://img.shields.io/badge/status-discontinued-lightgrey)](https://github.com/appsec-foundry/tss-web)
[![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](https://github.com/appsec-foundry/tss-web/blob/main/LICENSE)

[**tss-web**](https://github.com/appsec-foundry/tss-web) is an open security requirements framework for web applications and services.

- Covers technical and organizational controls for developing and operating web applications.
- Sits between high-level security policies such as ISO/IEC 27001 and technology-specific secure-coding guidelines.
- No longer maintained.

---

Questions and bug reports are welcome in each project's issue tracker.

**Maintainer:** Matthias Rohr &nbsp;<a href="https://www.linkedin.com/in/matthias-rohr/"><img src="https://raw.githubusercontent.com/appsec-foundry/.github/main/profile/images/linkedin.png" alt="" height="16" align="absmiddle"> LinkedIn</a>
