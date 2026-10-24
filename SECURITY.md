# Security policy

Security fixes target the latest released version. This is a small desktop project without a promised response time or security certification.

## Report a vulnerability

If this repository has private vulnerability reporting enabled, open its **Security** tab, select **Advisories**, then **Report a vulnerability**. Reports submitted there are private. Include the affected version, impact, and minimal reproduction steps using disposable files and made-up paths. Do not include personal files, credentials, your application database or raw logs.

If that button is absent, private reporting has not been enabled or is unavailable. Do not post exploit details in a public issue. Ask the repository owner to establish a private reporting channel first; a public request should contain no vulnerability details. No private contact address is currently declared in this source distribution.

Maintainers should enable the feature according to [GitHub's private reporting instructions](https://docs.github.com/en/code-security/how-tos/report-and-fix-vulnerabilities/configure-vulnerability-reporting/configure-for-a-repository). A policy file alone does not enable it.

## Scope and limits

TidyDesk sorts files locally according to configured rules. It does not execute, install, mount, unpack or scan files for malware. File classification is not a safety judgment. Preview moves first, keep backups, and test new rules on a disposable folder.

App state and logs can contain local filenames and paths. Keep them private. Do not commit application profiles, databases, logs or screenshots of personal folders.

Dependency audits check published vulnerability advisories and may miss unknown issues. The source export's targeted credential/path checks also need human review. Neither constitutes antivirus protection or an independent security audit.

Builds produced by the supplied build script are not code-signed. SHA-256 checksums detect changes when compared with a trusted checksum; they do not authenticate the publisher. Never disable Windows security checks to run an unfamiliar download.
