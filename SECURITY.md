# Security policy

lernapps apps are used by children. We take reports about security and privacy seriously.

## Reporting a vulnerability

**Please do not open a public issue.** Report privately through GitHub:

1. Go to the **Security** tab of the affected repository.
2. Click **Report a vulnerability**.

If you don't know which repository is affected, report it in [lernapps/.github](https://github.com/lernapps/.github/security/advisories/new).

We confirm receipt within a week and keep you informed about the fix.

## What counts

Besides classic vulnerabilities (e.g. script injection), please report anything that breaks our privacy promise, for example:

- a page that sends a request to a third-party server before the user clicks something,
- a tracker, cookie or analytics call,
- a way to make an AI tutor prompt (`tutor.md`, `llms.txt`) point learners to foreign content,
- learner data leaving the device.

## Supported versions

All sites are deployed continuously from `main`. Only the current version is supported.
