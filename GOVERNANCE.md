# Governance

How decisions are made in the lernapps organisation. Background and reasoning: [ORGANIZATION.md §5](ORGANIZATION.md#5-governance-and-community).

## Owners

The organisation has two owners with equal rights: **Oliver Jägle** ([@mrsimpson](https://github.com/mrsimpson)) and **Ralf D. Müller** ([@raifdmueller](https://github.com/raifdmueller)).

- Both co-own every **common repo**: `.github`, `lernapps.github.io`, `map`, `docs`, `tooling`, `app-template`. Neither leads a common repo alone; CODEOWNERS names the team, not a person.
- **App repos** belong to their authors. `mathe-karte` is Ralf's app. The org owners keep admin rights on every repo for security and emergencies, but do not decide about an app's content.

## Roles

| Role | Who | Can |
|---|---|---|
| Maintainer (team `maintainers`) | the owners | everything in the common repos; org settings; releases |
| Map editor (team `map-editors`) | the owners, later teachers | decide which capabilities are on the map |
| App author (team `app-authors`) | authors of curated apps | write to their own app repo |
| Reviewer (team `reviewers`) | the owners and AI-review accounts | review across repos |
| Contributor | anyone | issues, pull requests, discussions |

**Path to more rights:** after three merged pull requests, a contributor can be invited as app author or map editor. Both owners must agree.

## How decisions are made

| Kind of decision | Where | Who decides |
|---|---|---|
| Inside one repo | an ADR or the PR in that repo | the repo's owners (for apps: the author) |
| Affecting several repos (protocols, license, naming, reserved paths, tooling policy) | an ADR in `docs` (until it exists: an issue labelled `decision` in `.github`) | **both owners** |
| Changes to the map model (new top-level areas, new fields) | an issue labelled `rfc` in `map`, open for at least 7 days | the map editors |
| Everyday changes to common repos | a pull request | one approving review by the other owner |

If the owners disagree, the current state stays until they agree. Nobody merges their own change to a common repo without the other's review, except to fix something that is broken for learners right now; such a change is reviewed afterwards.

## Changing this document

Changes to this file need both owners to approve.
