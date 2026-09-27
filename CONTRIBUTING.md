# Contributing to lernapps

> **Kurz auf Deutsch:** Du musst nicht programmieren können, um beizutragen. Eine fehlende App, ein Fehler in einer Erklärung oder eine Idee: [lege ein Issue an](https://github.com/lernapps/.github/issues/new/choose), die Formulare sind auf Deutsch. Den Rest klären wir gemeinsam.

This file applies to every repository in the lernapps organisation that has no `CONTRIBUTING.md` of its own. App repos may add their own rules on top; `mathe-karte`, for example, has its own `CLAUDE.md`.

## Ways to contribute

| You want to … | Do this |
|---|---|
| report a gap: something learners should be able to do, with no good app for it | open a **gap report** issue |
| suggest an app | open an **app idea** issue |
| report a mistake in an app (wrong explanation, wrong feedback) | use the report link on the page, or open a **content error** issue in the app's repo |
| get your own app listed | open an **app registration** issue (the manifest protocol is being built, see [ORGANIZATION.md §3.2](ORGANIZATION.md#32-map-and-registry-the-manifest-protocol)) |
| change code or docs | open a pull request, see below |
| report a security problem | **do not** open an issue; see [SECURITY.md](SECURITY.md) |

## Pull requests

1. Open an issue first for anything bigger than a typo, so we can agree on the direction.
2. Work on a branch; one topic per PR.
3. Use [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, …).
4. CI must be green. Every site in the org is checked for: no external requests, readable without JavaScript, no broken links.
5. Common repos (`.github`, `lernapps.github.io`, `map`, `docs`, `tooling`, `app-template`) need one approving review by a maintainer. App repos follow their author's rules.

## Rules every contribution follows

- **Privacy by design.** No tracking, no cookies, no analytics, no requests to third-party servers before a user clicks. Learners are children.
- **Readable without JavaScript**, accessible (WCAG 2.1 AA), usable on a phone (360 px).
- **Language.** Common infrastructure (repo names, identifiers, schemas, workflows, developer docs) is in English. Text that learners, teachers and parents read is in German. Inside an app repo, the app's authors decide. See [ORGANIZATION.md §2](ORGANIZATION.md#2-language-and-naming-convention).
- **Decisions** that affect more than one repo are recorded as ADRs and need both owners to agree. See [GOVERNANCE.md](GOVERNANCE.md).

## License of contributions

Contributions are made under the license of the repository they go into ("inbound = outbound"). The license decision for the common repos is still open ([#19](https://github.com/lernapps/.github/issues/19)); the proposal is MIT for code and CC BY 4.0 for texts.

## Code of conduct

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md).
