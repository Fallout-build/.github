# Security Policy

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues, discussions, or pull requests.**

Report it privately through GitHub: go to the affected repository's **Security** tab and choose **Report a vulnerability**. That opens a private advisory visible only to you and the maintainers.

If you'd rather use email, or private reporting is unavailable on that repository, write to [security@fallout.build](mailto:security@fallout.build).

Either way, don't put details in a public issue.

Please include what you can:

- The affected repository, version, and platform.
- What an attacker can achieve, and what access they need to start.
- Steps to reproduce, ideally minimal.
- Any proof-of-concept, logs, or stack traces (as text).

## What to expect

- **Acknowledgement within 7 days.** If you don't hear back, please ping the advisory — don't assume it was received.
- We'll confirm the issue, work out which released versions are affected, and prepare a fix.
- We'll keep you updated as we go, and credit you in the advisory unless you'd rather stay anonymous.
- Fixes ship in a release, with a GitHub Security Advisory published for anything that warrants a CVE.

## Scope

Fallout is build automation: it executes your build definition, downloads tools, and handles credentials for publishing. Reports we're particularly interested in:

- Credential or token leakage — into logs, process argument lists, artifacts, or a packaged output.
- Arbitrary code execution triggered by untrusted input to the build (a crafted repository, tool manifest, or build graph).
- Tampering with the toolchain — dependency resolution or tool download that can be redirected or spoofed.
- Privilege escalation in CI, including anything that lets a fork's pull request reach secrets.

Out of scope: vulnerabilities in a build *you* wrote, findings that require an already-compromised machine, and reports against unsupported release lines. Automated scanner output without a demonstrated impact isn't usually actionable — tell us what an attacker gets.

## Supported versions

Security fixes go to the current production line, and to maintenance lines still receiving fixes. See each repository's branching and release documentation for which lines are live.
