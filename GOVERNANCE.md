# Governance

How decisions are made in the lernapps organisation. Overview of the org: [ORGANIZATION.md](ORGANIZATION.md).

The org is run by one person, so the rules are kept to a minimum. More roles and required reviews are added when more people join, not before. If the platform takes off, it could become a registered association (Verein), so that it belongs to those who fill it with life.

## Owner

**Oliver Jägle** ([@mrsimpson](https://github.com/mrsimpson)) is the sole owner of the organisation and accountable for the platform. He is in the team `maintainers`.

- He owns every **common repo**: `.github`, `lernapps.github.io`, `apps`, `docs`, `tooling`, `app-template`.
- **App repos** belong to their authors and follow their authors' rules. `mathe-karte` is the app of **Ralf D. Müller** ([@raifdmueller](https://github.com/raifdmueller)), who focuses on the apps and does not take part in the platform. The owner keeps admin rights on every repo for security and emergencies, but doesn't decide about an app's content.
- Only the owner creates repos.

## How changes are made

| Kind of change | How | Who decides |
|---|---|---|
| Everyday change to a common repo | A pull request that passes the required checks. A review is welcome, not required | whoever makes the change |
| Change affecting several repos (protocols, license, naming, reserved paths, tooling policy) | An issue labelled `decision` in `.github`, later an ADR in `docs` | **the owner** |
| Change inside an app | The app's own process | the app's author |

## Contributors

Anyone can open issues and pull requests. Contributors who stay get write access by invitation from the owner.

## Changing this document

Changes to this file are made by the owner, as a pull request, so they stay visible.
