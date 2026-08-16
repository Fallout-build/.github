# Support

## Getting help

- **Something's broken?** Open a bug report on the repository it affects.
- **Missing a capability?** Open a feature idea.
- **Not sure how something works?** Search existing and closed issues first — most questions have been asked once already.

Please don't email maintainers directly for support. Keeping it in issues means the next person with the same problem finds the answer.

## Which repository?

| It's about | Repository |
|---|---|
| Targets, dependencies, tool wrappers, the build engine, `dotnet fallout` | [Fallout](https://github.com/Fallout-build/Fallout) |
| The VS Code extension — Targets view, build graph, go-to-definition | [Fallout.Extensions.VSCode](https://github.com/Fallout-build/Fallout.Extensions.VSCode) |

When in doubt, file it against the framework and we'll move it.

## Before you file

Include the versions. Almost every unactionable report is missing them: the Fallout version, the .NET SDK version, your OS, and — for the extension — the VS Code and extension versions.

Paste logs and errors as text in a code block rather than as screenshots. Screenshots earn their place for genuinely visual problems (rendering, layout, theme contrast) and nowhere else.

## Security

Don't use issues for vulnerabilities. See [SECURITY.md](SECURITY.md).

## Coming from NUKE

Fallout is the hard-fork successor to [NUKE](https://github.com/nuke-build/nuke), under new maintenance since 2026. If you hit something that worked in NUKE 10.x and doesn't here, say so in the report — regressions against upstream are triaged ahead of most other work.
