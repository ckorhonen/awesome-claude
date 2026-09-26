# Repository instructions

`README.md` is the curated resource list; `contributing.md` controls eligibility and formatting. Preserve short descriptions, category placement, duplicate avoidance, attribution, and the documented one-project-per-PR convention for submissions. Verify changed resource claims from their actual source; do not infer current maintenance from an old list entry.

The root package provides `npm run lint` (awesome-lint) and `npm test` (the same lint command), so avoid duplicate runs. With Node/npm available, use the checked-in npm lockfile via `npm ci`; also preserve the existing pnpm lockfile. There is no root app build or typecheck. `npm run check-links` references a configuration file under `.github/workflows/` that is absent in this snapshot; report that prerequisite rather than presenting the command as ready or silently rewriting the workflow.

`claude-vscode-theme/` is a separate extension package: its manifest specifies Node >=20, VS Code >=1.80, and pnpm 9. Read its own README before work there; its commands are `pnpm build`, `pnpm compile` (tsc noEmit), `pnpm dev`, and `pnpm package`. Theme builds generate files and packaging is distinct from publishing. For prose-only edits, inspect links and run `git diff --check -- <changed-paths>`.

Complete the authorized change through relevant verification and repair of introduced failures. Resolve routine implementation choices directly; ask only for information or decisions that materially affect the result. If blocked, name the affected action and missing prerequisite, continue independent work, and close with changed paths, checks actually run, and unverified behavior.
