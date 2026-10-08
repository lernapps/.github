# Contributing to lernapps

> **Kurz auf Deutsch:** Du musst nicht programmieren können, um beizutragen. Eine App vorschlagen oder eintragen: [lernapps.net/apps/eintragen/](https://lernapps.net/apps/eintragen/). Ein Fehler in einer Erklärung oder eine Idee: lege ein Issue im passenden Repository an. Den Rest klären wir gemeinsam.

This file applies to every repository in the lernapps organisation that has no `CONTRIBUTING.md` of its own. App repos may add their own rules on top; `mathe-karte`, for example, has its own `CLAUDE.md`.

## Ways to contribute

| You want to … | Do this |
|---|---|
| report a mistake in an app (wrong explanation, wrong feedback) | use the report link on the page, or open an issue in the app's repo |
| suggest an app or get your own app listed | follow [lernapps.net/apps/eintragen/](https://lernapps.net/apps/eintragen/), or open an **App eintragen** issue in [`apps`](https://github.com/lernapps/apps/issues/new/choose) |
| change code or docs | open a pull request, see below |
| report a security problem | **do not** open an issue; see [SECURITY.md](SECURITY.md) |

## Pull requests

1. Open an issue first for anything bigger than a typo, so we can agree on the direction.
2. Work on a branch; one topic per PR.
3. Use [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, …).
4. CI must be green. Every site in the org is checked for: no external requests, readable without JavaScript, no broken links.
5. A maintainer merges it. App repos follow their author's rules.

## Rules every contribution follows

- **Privacy by design.** No tracking, no cookies, no analytics, no requests to third-party servers before a user clicks. Learners are children.
- **Readable without JavaScript**, accessible (WCAG 2.1 AA), usable on a phone (360 px).
- **Language.** Common infrastructure (repo names, identifiers, schemas, workflows, developer docs) is in English. Text that learners, teachers and parents read is in German. Inside an app repo, the app's authors decide. See [ORGANIZATION.md](ORGANIZATION.md#rules-across-repos).
- **Decisions** that affect more than one repo are made in an issue labelled `decision` and are decided by the owner. See [GOVERNANCE.md](GOVERNANCE.md).

## License of contributions

Contributions are made under the license of the repository they go into ("inbound = outbound"). Each repo has one license, named in its `LICENSE` file: MIT for code and app repos, CC BY-SA 4.0 for the text repos `.github` and `docs`. There is no CLA. Third-party content (quotes, images, texts from Wikipedia) keeps its own license: name the source and the license where you use it.

## Code of conduct

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md).
