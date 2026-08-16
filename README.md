# .github

Org-wide defaults for [Fallout-build](https://github.com/Fallout-build). Nothing here is a project — it's the one copy of the files every repository would otherwise duplicate.

`profile/README.md` is the org landing page. Most of the rest are **default community health files**: GitHub serves them for any repository in the org that doesn't ship its own.

[`costs.md`](costs.md) is the exception — a plain document that lives here because project spend is an org concern rather than a code one. GitHub has no inheritance mechanism for it, so repositories link to it rather than receiving it automatically.

## What's inherited

| File | Applies to |
|---|---|
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Every repo |
| [`SECURITY.md`](SECURITY.md) | Every repo — vulnerability reporting goes through each repo's **Security** tab |
| [`SUPPORT.md`](SUPPORT.md) | Every repo — where to file, and what to include |
| [`.github/FUNDING.yml`](.github/FUNDING.yml) | Sponsor button |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Generic bug / feature forms, as a floor for repos without their own |

Plus [`costs.md`](costs.md), linked rather than inherited — see above.

**A repository's own copy always wins.** GitHub looks in that repo's `.github/`, then its root, then `docs/`, and only falls back here. So a repo with specific needs — the VS Code extension asks for a `build-graph.json` slice, which would be meaningless elsewhere — just ships its own file and the default steps aside. The templates here are the floor, not the ceiling.

Deleting a repo's local copy is what activates the default. Adding a file here does nothing to a repo that still has its own.

## What can't live here

Not everything is inheritable, and some things only look like they should be:

- **`LICENSE`** — explicitly excluded by GitHub. Every repo carries its own.
- **`CODEOWNERS`** — not a community health file, and inherently per-repo since it maps paths.
- **`.github/release.yml`** — repo config, not a health file. The label taxonomy is deliberately kept identical across repos by convention instead.
- **Workflows** — not inheritable. Share CI through [reusable workflows](https://docs.github.com/actions/using-workflows/reusing-workflows) called from each repo.
- **`CONTRIBUTING.md`** — inheritable in principle, kept per-repo in practice: the branch models genuinely differ (the framework has no `develop`; the extension does), so one shared copy would have to lie to one of them.
- **`AGENTS.md` / `CLAUDE.md`** — not a GitHub mechanism at all. AI tools read these from the working tree, so they can't be inherited. Each repo keeps its own canonical brief, with `CLAUDE.md` pointing at it.

## Reference

[Creating a default community health file](https://docs.github.com/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
