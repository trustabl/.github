# Contributing to Trustabl

Thanks for helping. This guide covers every repository in the trustabl
organization. A repository with its own `CONTRIBUTING.md` (for example the
[analyzer](https://github.com/trustabl/agent-reliability-analyzer)) adds the
build and test steps for that code; read it too.

## Questions and ideas

Ask in the [Trustabl Discord](https://discord.gg/G6gM8nKxPg). For a feature
idea, open an issue with the feature request template so the discussion has a
home.

## Reporting a bug

Open an issue with the bug report template. Include the version
(`trustabl version`, or the package version), your platform, the smallest
input that reproduces the problem, and what you expected instead.

**Security problems are not bugs to file in public.** Follow
[SECURITY.md](SECURITY.md) instead.

## Pull requests

- Open an issue first for anything larger than a small fix, so we can agree on
  the approach before you write the code.
- Keep each pull request to one change, with tests that fail without it.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/)
  (`fix(rulesource): ...`, `feat(rules): ...`, `docs: ...`).
- Add user-visible changes to the `Unreleased` section of `CHANGELOG.md` where
  the repository has one.
- CI must pass before a maintainer reviews.

## Repositories

| Repository | What it is |
|---|---|
| [agent-reliability-analyzer](https://github.com/trustabl/agent-reliability-analyzer) | The `trustabl` CLI and MCP server (Go) |
| [agent-reliability-rules](https://github.com/trustabl/agent-reliability-rules) | The detection rules the analyzer downloads (YAML) |
| [agent-reliability-skills](https://github.com/trustabl/agent-reliability-skills) | Trustabl Forge: pre-coding reliability skills (MCP server) |
| [agent-network-access-probe](https://github.com/trustabl/agent-network-access-probe) | Trustabl Probe: network-access testing for agents |

A rule change touches two repositories: the rule in agent-reliability-rules
and its test mirror in the analyzer's `testdata/rules-fixture/`. Open both pull
requests and link them; they are merged together.

## License

By contributing, you agree that your contribution is licensed under the
license of the repository you contribute to (Apache-2.0 for the repositories
above).

## Code of conduct

Everyone taking part follows our [Code of Conduct](CODE_OF_CONDUCT.md).
