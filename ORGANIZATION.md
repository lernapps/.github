# How the lernapps organisation works

lernapps.net collects small, free learning apps for school: static, without accounts and without tracking. Why it exists is in the [org profile](profile/README.md) (German). This page says where things are, who to reach and which rules hold across repos.

## Where to find what

| Repo | Served at | What's in it | Owner |
|---|---|---|---|
| [`.github`](https://github.com/lernapps/.github) | – | This page, org profile, [CONTRIBUTING](CONTRIBUTING.md), [GOVERNANCE](GOVERNANCE.md), [SECURITY](SECURITY.md), [SUPPORT](SUPPORT.md), [Code of Conduct](CODE_OF_CONDUCT.md); cross-repo work and decisions as issues | Oliver |
| [`lernapps.github.io`](https://github.com/lernapps/lernapps.github.io) | [lernapps.net](https://lernapps.net/) | Home page, [privacy notice](https://lernapps.net/privacy/), [imprint](https://lernapps.net/imprint/), forwarding of old addresses | Oliver |
| [`apps`](https://github.com/lernapps/apps) | [lernapps.net/apps/](https://lernapps.net/apps/) | The app overview: find a learning app, list your own; one entry per app | Oliver |
| [`docs`](https://github.com/lernapps/docs) | [lernapps.net/docs/](https://lernapps.net/docs/) | Vision, the organisation (biz42), the platform design (pdt42), later cross-repo ADRs | Oliver |
| [`tooling`](https://github.com/lernapps/tooling) | – | Shared checks and reusable workflows (being built) | Oliver |
| [`app-template`](https://github.com/lernapps/app-template) | – | Starting point for a new app (being built) | Oliver |
| [`mathe-karte`](https://github.com/lernapps/mathe-karte) | [lernapps.net/mathe-karte/](https://lernapps.net/mathe-karte/) | The Mathe-Karte: maths for Sek I with trainers and an AI tutor; the reference app | Ralf |

Oliver Jägle ([@mrsimpson](https://github.com/mrsimpson)) is the owner of the organisation and accountable for the platform. Ralf D. Müller ([@raifdmueller](https://github.com/raifdmueller)) is the author of the Mathe-Karte. Details in [GOVERNANCE.md](GOVERNANCE.md).

## How to reach us

| You want to … | Go to |
|---|---|
| suggest an app or get your app listed | [lernapps.net/apps/eintragen/](https://lernapps.net/apps/eintragen/), or an issue in [`apps`](https://github.com/lernapps/apps/issues/new/choose) |
| report an error in an app | an issue in that app's repo |
| report a security or privacy problem | privately, as described in [SECURITY.md](SECURITY.md) |
| discuss the organisation, its rules or plans | an issue in [`.github`](https://github.com/lernapps/.github/issues) |
| contact the owner directly | [lernapps@beimir.net](mailto:lernapps@beimir.net) |

## Rules across repos

**Structure**
- One repo per app, one repo per shared concern. No monorepo of apps.
- Repo names are paths: a repo `x` with Pages is served at `lernapps.net/x/`. Only the owner creates repos.
- A document about one repo lives in that repo. A document about how repos relate lives in `docs`.

**Apps and the app overview**
- An app connects to the platform in one way only: its entry in the app overview links to it. Nothing embeds an app, and apps share no code at runtime.
- One entry per app: a YAML file in `apps/entries/`, checked against the entry schema. The owner decides whether an app is listed.
- What an app contains, such as trainers, is the app's own business.
- How the platform is meant to work is the [platform design](https://lernapps.net/docs/platform-design/) in `docs`.

**Every page, in every repo**
- No cookies, no tracking, no requests to other servers before a click. The [privacy notice](https://lernapps.net/privacy/) states these rules for all of lernapps.net; anything beyond them needs the notice changed first.
- Readable without JavaScript, WCAG 2.1 AA, usable at 360 px.
- Links to the [imprint](https://lernapps.net/imprint/) and the [privacy notice](https://lernapps.net/privacy/).

**Language**
- Shared infrastructure is in English: repo names, identifiers, schemas, workflows, the manifest, developer docs.
- Text for learners, teachers and parents is in German.
- Inside an app repo, its author decides. The Mathe-Karte uses German names internally.

**Pipelines**
- Every change to a default branch goes through a pull request with the repo's required checks.
- Actions are pinned to a full commit SHA; Dependabot updates them.

## License

One license per repo, in its `LICENSE` file:

| Repos | License |
|---|---|
| Code and app repos: `lernapps.github.io`, `apps`, `tooling`, `app-template`, `mathe-karte`, every app | MIT, including the texts in them |
| Text repos: `.github`, `docs` | CC BY-SA 4.0 |

Contributions come under the repo's license. Third-party content an app uses (quotes, images, texts from Wikipedia) keeps its own license; the app names source and license next to it.

## Decisions and governance

- One owner; no required reviews. Details in [GOVERNANCE.md](GOVERNANCE.md).
- Decisions inside a repo: in that repo, e.g. as ADRs.
- Decisions across repos: an issue labelled [`decision`](https://github.com/lernapps/.github/issues?q=label%3Adecision) in `.github`; the owner decides.

## What's being worked on

The plan lives in the [issues and milestones](https://github.com/lernapps/.github/milestones) of this repo. The main threads:

- **Tooling:** shared checks and workflows, taken from the Mathe-Karte ([#5](https://github.com/lernapps/.github/issues/5)).
- **App overview:** the first-draft MVP of the [platform design](https://lernapps.net/docs/platform-design/), in [`apps`](https://github.com/lernapps/apps).
- **Making apps:** app template and a guide for contributors ([#12](https://github.com/lernapps/.github/issues/12), [#33](https://github.com/lernapps/.github/issues/33)).
- **Open decisions:** [label `decision`](https://github.com/lernapps/.github/issues?q=is%3Aopen+label%3Adecision).

## History

The organisation took this shape on 27–28 September 2026. It brought together `mrsimpson/edugo` (the why and the map, now `docs` and `map`) and Ralf's Mathe-Karte, which used to be served at the root and moved to `/mathe-karte/`. Old addresses keep working. In October 2026 the platform design replaced the map with the app overview in `apps`; `map` is being retired. Since then Oliver is the sole owner, and Ralf focuses on the Mathe-Karte. The full planning document from that time, with the reasoning behind the rules above, is [ORGANIZATION.md as of 2026-09-28](https://github.com/lernapps/.github/blob/2c772917a440c21d2e1bcff15930eb9d24aef177/ORGANIZATION.md).
