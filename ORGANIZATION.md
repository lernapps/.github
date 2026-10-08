# How the lernapps organisation works

**lernapps.net gets small learning apps into use.** Free to use, kept alive by thanks: adults and students find an active-learning app they can use right away, without doubt about whether it may be used; creators list theirs with almost no effort and hear when it helped. A thank-you, free and anonymous, is what keeps the platform alive. (The narrative of the [platform design](https://lernapps.net/docs/platform-design/), D1 `platform-lernapps`.)

This page says which repo does what for that story, who to reach and which rules hold across repos. Why it exists, in German: the [org profile](profile/README.md).

**Agents, start here.** Then read the platform design with the skill [`skills/pdt`](https://github.com/lernapps/docs/tree/main/skills/pdt) in `docs`. Every repo's README says which part of the design it serves; change the design only in `docs`.

## Where to find what

| Repo | Served at | What it does for the platform (platform design) | Owner |
|---|---|---|---|
| [`lernapps.github.io`](https://github.com/lernapps/lernapps.github.io) | [lernapps.net](https://lernapps.net/) | The home page: the story for teachers, parents, creators and learners (D1); [privacy notice](https://lernapps.net/privacy/), [imprint](https://lernapps.net/imprint/), the brand. Also the **shared site frame** of all sites (design tokens, header, footer, deploy check) | Oliver |
| [`apps`](https://github.com/lernapps/apps) | [lernapps.net/apps/](https://lernapps.net/apps/) | The app overview, the core of the MVP (D8): find an app, see that it may be used, bring it to class, say thanks (`x-app-in-minutes`, `x-practice-tonight`); list an app and hear back (`x-list-and-hear-back`). One entry per app in `entries/` | Oliver |
| [`docs`](https://github.com/lernapps/docs) | [lernapps.net/docs/](https://lernapps.net/docs/) | The design itself: vision, the organisation (biz42), the platform design (pdt42), the `pdt` skill for agents; later cross-repo ADRs | Oliver |
| [`tooling`](https://github.com/lernapps/tooling) | – | GitHub as the means of production (D1): the site actions every site builds, checks and deploys with, the Renovate preset of all repos; later the guidance for building apps (D6 `s-building-guidance`) | Oliver |
| [`app-template`](https://github.com/lernapps/app-template) | – | Starting point for a new app (D6 `s-building-guidance`; being built) | Oliver |
| [`mathe-karte`](https://github.com/lernapps/mathe-karte) | [lernapps.net/mathe-karte/](https://lernapps.net/mathe-karte/) | The first app (D8 `mvp-first-draft`): maths for Sek I with trainers and an AI tutor | Ralf |
| [`.github`](https://github.com/lernapps/.github) | – | This page, org profile, [CONTRIBUTING](CONTRIBUTING.md), [GOVERNANCE](GOVERNANCE.md), [SECURITY](SECURITY.md), [SUPPORT](SUPPORT.md), [Code of Conduct](CODE_OF_CONDUCT.md), the issue chooser; cross-repo work and decisions as issues | Oliver |

Oliver Jägle ([@mrsimpson](https://github.com/mrsimpson)) is the owner of the organisation and accountable for the platform. Ralf D. Müller ([@raifdmueller](https://github.com/raifdmueller)) is the author of the Mathe-Karte. Details in [GOVERNANCE.md](GOVERNANCE.md).

## What every site shares

All sites on lernapps.net (home, `/apps/`, `/docs/`, and apps that want to) look and behave the same:

- **Look:** design tokens, header with the common navigation, and footer come from [`site-frame/`](https://github.com/lernapps/lernapps.github.io/tree/main/site-frame) in `lernapps.github.io`, used as the npm package `@lernapps/site` straight from git (not published).
- **Build and deploy:** `npm ci`, `npm run build` into `_site/`, `npm run check` (`lernapps-check`); `main` is published to the repo's `gh-pages` branch, each pull request gets a preview under `pr-preview/pr-<n>/`. The steps are the site actions in [`tooling`](https://github.com/lernapps/tooling); the repos only call them.
- **Updates:** every repo's `renovate.json` extends `github>lernapps/tooling`. Renovate bumps the site frame and the actions to the latest commit of their `main` and merges when green, so a change there reaches every site.

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
- Shared infrastructure is in English: repo names, identifiers, schemas, workflows, developer docs.
- Text for learners, teachers and parents is in German.
- Inside an app repo, its author decides. The Mathe-Karte uses German names internally.

**Pipelines**
- Every change to a default branch goes through a pull request with the repo's required checks.
- Actions are pinned to a full commit SHA; Renovate updates them (Dependabot in `mathe-karte`).

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

The plan lives in the [issues](https://github.com/lernapps/.github/issues) of this repo, and in the repo concerned. The main threads:

- **The first draft of the MVP** (D8 `mvp-first-draft`): the app overview in [`apps`](https://github.com/lernapps/apps), the first creators, the anonymous thanks.
- **Checking listed apps** before the real MVP: an agent clicks through each app, records the network and reviews the source ([docs#1](https://github.com/lernapps/docs/issues/1)).
- **Guidance for building apps** (D6 `s-building-guidance`): agent skill and app template ([#12](https://github.com/lernapps/.github/issues/12)).
- **Open decisions:** [label `decision`](https://github.com/lernapps/.github/issues?q=is%3Aopen+label%3Adecision).

## History

The organisation took this shape on 27–28 September 2026. It brought together an earlier platform idea around a capability map and Ralf's Mathe-Karte, which used to be served at the root and moved to `/mathe-karte/`. Old addresses keep working. In October 2026 the platform design replaced the capability map with the app overview in `apps`; `map` is archived. Since then Oliver is the sole owner, and Ralf focuses on the Mathe-Karte. The full planning document from that time, with the reasoning behind the rules above, is [ORGANIZATION.md as of 2026-09-28](https://github.com/lernapps/.github/blob/2c772917a440c21d2e1bcff15930eb9d24aef177/ORGANIZATION.md).
