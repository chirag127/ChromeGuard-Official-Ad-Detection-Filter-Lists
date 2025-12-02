# Security Policy for ChromeGuard-Official-Ad-Detection-Filter-Lists

As the Apex Technical Authority, we treat security with the highest priority, adhering to a **Zero-Defect** mandate across all archival and active projects. This repository, housing critical web standards enforcement data, is managed under rigorous 2025/2026 security protocols.

## 1. Supported Versions

This repository primarily contains configuration data (filter lists) and infrastructure configuration files (YAML, Markdown). These are generally static and immutable artifacts. We focus our active patching efforts on the direct CI/CD pipeline configuration (`.github/workflows/ci.yml`) and dependency resolution where applicable (e.g., tooling used in CI).

All active workflows are configured to use audited, stable toolchains as defined in the `AGENTS.md` directives.

## 2. Vulnerability Reporting

We strongly encourage security researchers to report vulnerabilities responsibly.

If you discover a security vulnerability in this repository (e.g., in configuration files that could lead to supply chain risks, insecure workflow execution, or accidental data leakage), please follow these steps:

1.  **Do not** open a public Issue.
2.  Email the security team directly using the designated security contact channel (since this is an archival project, we default to a general security contact format):
    *   **Email:** `security+chirag127@users.noreply.github.com` (GitHub's standard practice for private disclosure)
3.  In your email, clearly describe the vulnerability, the affected file(s), and steps to reproduce the issue.

We aim to acknowledge receipt of the report within **48 hours**.

## 3. Patching and Response Timeline

Upon confirmation of a valid vulnerability, the response priority is dictated by potential impact:

| Severity | Response Goal | Resolution Goal |
| :--- | :--- | :--- |
| **Critical** | Immediate halt of relevant CI/CD pipelines. | Fix deployed within 72 hours. |
| **High** | Triage and root cause analysis initiated. | Fix deployed within 7 days. |
| **Medium/Low** | Scheduled for the next maintenance cycle (typically bi-weekly). | Fix deployed within 30 days. |

For this **Filter List Archive**, high-priority fixes primarily involve remediation of workflow configurations that could allow unauthorized execution or external contamination.

## 4. Security Scanning & Auditing

This repository adheres to the Apex requirement for continuous verification:

*   **Dependency Scanning:** While this repository is configuration-heavy, the underlying GitHub Actions runners are subject to [GitHub Dependency Scanning](https://docs.github.com/en/code-security/dependabot/managing-vulnerabilities-with-the-container-and-dependency-graph).
*   **Static Analysis:** All custom scripts or infrastructure-as-code definitions are validated by the standards enforced via the `.github/workflows/ci.yml` pipeline, utilizing tools aligned with 2026 best practices (e.g., secure execution context validation).

--- 
*Last Updated: December 2025, Enforced by Apex Technical Authority.*