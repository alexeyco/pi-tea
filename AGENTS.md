# pi-tea

Forgejo/Gitea skill for the pi coding agent, published as a pi package.
Human-facing docs: [README.md](README.md), [CONTRIBUTING.md](CONTRIBUTING.md).

## Layout

- `skills/tea/SKILL.md` — the skill; pi loads it via the `pi.skills` manifest in `package.json`.
- `package.json` — npm metadata + pi manifest; keep the `pi-package` keyword (gallery discoverability).

## Conventions

- Docs and comments in English.
- `SKILL.md` must stay instance-agnostic: no hard-coded hostnames or URLs.
- `SKILL.md` description (frontmatter) is what pi shows the agent — keep it short.
- Never push `master`; work on feature branches, merge via PR.

## Release

Tag-driven npm publish — see [CONTRIBUTING.md](CONTRIBUTING.md#publishing) and `.github/workflows/publish.yml`.
