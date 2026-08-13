# Contribution Guidelines

Thanks for your interest in contributing to **Awesome SysML v2**! 🎉

This is a curated list following the
[Awesome manifesto](https://github.com/sindresorhus/awesome/blob/main/awesome.md).
Please read these guidelines carefully before opening a pull request.

## Adding something to the list

You will need a [GitHub account](https://github.com/join). If you are new
to GitHub, see [First Contributions](https://github.com/firstcontributions/first-contributions).

1. Open `README.md` and click the **edit** (pencil) icon.
2. Find the appropriate section in the `## Contents` list. **Do not** invent
   a new top-level section without also updating `## Contents`.
3. Add your entry at the **bottom** of the relevant bulleted list,
   matching the existing pattern: `- [Name](URL) - Description.`
4. Run `awesome-lint` locally and fix any reported issues before committing:

   ```bash
   npx awesome-lint
   ```

5. Open the pull request with a short title describing the addition
   (e.g. `Add sysml-v2-foo`). Don't prefix it with "Awesome".

## What makes an entry "awesome"

- **Curation, not collection.** Only add items you can *personally
  recommend*. "Only awesome is awesome" — when in doubt, leave it out.
- The project must have **real documentation** and be **maintained**.
  Unmaintained, archived, or deprecated projects belong in
  `CANDIDATES.md`, **not** in `README.md`.
- The project should be **directly useful** to people working with
  SysML v2 / KerML — tools, libraries, samples, syntax highlighting,
  editors, or commercial products in this space.

## Format requirements for an entry

Each entry is a single bulleted list item in the form:

```md
- [Name](URL) - Description.
```

The description must:

- start with an **uppercase** character,
- end with a **period** (`.`),
- explain **why** the item is useful, not just restate the name as a tagline,
- use **consistent, correct naming** (e.g. `VS Code`, `Jupyter`, `Python`,
  `TypeScript`, `Node.js` — not `VSCode` or `node.js`),
- be **grammatically correct** and free of typos.

### Link hygiene

- Prefer the canonical repo URL: `https://github.com/owner/repo`.
- If the project has its own site, include it parenthetically, e.g.
  `([Site](https://example.com))`, matching the pattern already used in
  that section.
- Don't link to forks or mirrors when the upstream is available.
- Ensure the link resolves (run `curl -sI` if unsure). If a previously
  listed repo is gone, open an issue or PR to fix it rather than leaving a
  broken link.

## Updating your pull request

A maintainer may ask you to edit your PR before it's merged — usually for
formatting, spelling, or compliance with these guidelines. See
[Amending a Commit Guide](https://github.com/RichardLitt/knowledge/blob/master/github/amending-a-commit-guide.md)
for how to update a pull request.

## Repository structure

| File | Purpose |
|------|---------|
| `README.md` | The published Awesome list. **Only** items that have been personally reviewed. |
| `CANDIDATES.md` | Working scratchpad of unvetted GitHub search results. Promote from here to `README.md` only after review. |
| `AGENTS.md` | Internal guidance for AI agents and contributors — not part of the published list. |
| `LICENSE` | CC0-1.0. Do not add a "License" section to the readme; GitHub renders it from this file. |

## Unmaintained / deprecated / archived items

Per the Awesome guidelines, items that are unmaintained, archived, or
deprecated should **not appear in `README.md`**. Track them in
`CANDIDATES.md` under a clear "Moved / deprecated" heading with the reason.

## Need help?

- Open an issue for discussion before a large PR.
- For questions about scope, ping a maintainer in your PR description.

Thanks for helping make this list awesome! 😎
