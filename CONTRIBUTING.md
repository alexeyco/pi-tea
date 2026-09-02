# Contributing

## Branching

- Never push to `master`.
- Branch from `master`: `git checkout -b feat/<topic>`.
- Commit messages: no conventional prefixes (`feat:`, `fix:`, …), past tense —
  e.g. `Added tea skill`, `Fixed setup section`.

## Development

Edit `skills/tea/SKILL.md` — pi picks it up on the next session or `/reload`.
Test locally without publishing (local installs are not copied, edits are live):

```sh
pi install /absolute/path/to/pi-tea
```

Format with `make fmt` (prettier). Run the sanity checks before committing —
same as CI:

```sh
make check
```

## Publishing

1. Add a `CHANGELOG.md` entry for the new version.
2. Bump `version` in `package.json` (semver).
3. Merge the PR to `master`.
4. Tag and push the tag:

   ```sh
   git tag vX.Y.Z && git push origin vX.Y.Z
   ```

5. The `publish` workflow (.github/workflows/publish.yml) runs `npm publish` on tag push.
   Requires the `NPM_TOKEN` secret in the repo settings.

Install for users:

```sh
pi install npm:pi-tea          # latest
pi install npm:pi-tea@0.1.0    # pinned
```
