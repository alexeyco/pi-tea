# @alexeyco/pi-tea

> **Deprecated** — this package has been renamed to
> [`@alexeyco/tea`](https://www.npmjs.com/package/@alexeyco/tea). Install the
> new package instead:
>
> ```sh
> pi install npm:@alexeyco/tea
> ```
>
> `@alexeyco/pi-tea` will not receive any further updates.

[Forgejo](https://forgejo.org) / [Gitea](https://gitea.io) skill for the [pi](https://pi.dev) coding agent.

Teaches the agent to drive the [`tea`](https://gitea.com/gitea/tea) CLI: browse repos, issues, pulls, releases, branches, comments and notifications. Read-only by default; anything state-changing requires explicit confirmation.

<p align="center">
  <img src="docs/gallery/terminal.png" alt="@alexeyco/pi-tea demo" width="640">
</p>

## Install

Deprecated — install the renamed package instead:

```sh
pi install npm:@alexeyco/tea
```

Requires the `tea` CLI and a configured login (`tea login add`).

## Usage

Ask in natural language; pi loads the skill when relevant:

- “List open issues in `owner/repo`, most recent first.”
- “Summarize PR #42, including the comments.”
- “What’s in the latest release of `owner/repo`?”
- “Any unread notifications?”

State-changing actions (commenting, creating issues, merging) are proposed
as exact commands and run only after you confirm.

## See also

- [CONTRIBUTING.md](CONTRIBUTING.md) — development and release workflow.
