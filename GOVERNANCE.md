# Governance

How decisions are made in the lernapps organisation. Overview of the org: [ORGANIZATION.md](ORGANIZATION.md).

The org is run by two people who trust each other, so the rules are kept to a minimum. More roles and required reviews are added when more people join, not before.

## Owners

The organisation has two owners with equal rights: **Oliver Jägle** ([@mrsimpson](https://github.com/mrsimpson)) and **Ralf D. Müller** ([@raifdmueller](https://github.com/raifdmueller)). Both are in the team `maintainers`.

- Both co-own every **common repo**: `.github`, `lernapps.github.io`, `map`, `docs`, `tooling`, `app-template`.
- **App repos** belong to their authors and follow their authors' rules. `mathe-karte` is Ralf's app. The owners keep admin rights on every repo for security and emergencies, but don't decide about an app's content.
- Only the owners create repos.

## How changes are made

| Kind of change | How | Who decides |
|---|---|---|
| Everyday change to a common repo | A pull request that passes the required checks. A review by the other owner is welcome, not required | whoever makes the change |
| Change affecting several repos (protocols, license, naming, reserved paths, tooling policy) | An issue labelled `decision` in `.github`, later an ADR in `docs` | **both owners** |
| Change inside an app | The app's own process | the app's author |

If the owners disagree on a decision, the current state stays until they agree.

## Contributors

Anyone can open issues and pull requests. Contributors who stay get write access by invitation, when both owners agree.

## Changing this document

Changes to this file need both owners to agree.
