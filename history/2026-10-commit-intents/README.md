# Commit intents of the platform repos, 2026-10

On 2026-10-22 the history of `main` in tooling, app-templates, apps, docs, lernapps.github.io and .github was
rewritten. Most commits of the agentic app-creation increment (2026-09-29 to 2026-10-22) said what changed but not
why; the why was only in the Claude Code sessions that made them. Each commit from a session now carries its intent.

How it was done is the skill
[commit-intents](https://github.com/mrsimpson/skills-coding/tree/main/commit-intents) (with
[claude-code-sessions](https://github.com/mrsimpson/skills-coding/tree/main/claude-code-sessions)), worked out in the
session https://claude.ai/code/session_01CokaJ6YdJLqEGhHnk4MHJp.

## What changed in the repos

- Only commits with a `Claude-Session:` trailer, and the merges that bring them in, got new messages: a conventional
  subject, then Intent, Key changes and, where it applies, Dependencies and side effects. Bot commits and commits
  without a session kept theirs.
- Commits that follow each other directly on one branch and serve the same thought became one commit: 588 commits
  from 28 sessions became 444. Every tree, author, committer and time is kept; nothing was reordered; the final tree
  of each repo is identical.
- The old `main` of each repo is the branch `archive/pre-rewrite`, so every old SHA still resolves: pins in the apps,
  SHAs in issues, pull requests and eval results.

## The files

| File | What it holds |
|---|---|
| `view/index.html` | The review page: one card per intent with time, proposed commit, intent, key decisions, source commits and repos. Open it in a browser. |
| `data/commits.json` | The inventory: every commit in scope with parents, times, message, files, session, and which commit a plan commit joins. |
| `data/intents.json` | The first cut by time: per session, the person's messages since the last commit and the commits after them. |
| `data/written/<id>.json` | The written intents, the source of the new messages: why, key decisions, trigger, squash groups with their messages, and every commit placed differently from the first cut (`moved`). |
| `data/session-parents.json` | Sessions another session created, with the prompt they got. |
| `data/slices.json` | The time slices the agents worked on. |
| `data/sha-map-<repo>.json` | Old SHA → new SHA for every commit of `main`. |

The serialized session texts are not here: they hold the person's whole conversations. They can be drawn again from
the sessions with the skill `claude-code-sessions`.
