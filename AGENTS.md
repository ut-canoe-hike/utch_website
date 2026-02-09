# AGENTS

## Workflow
- Proactively check `git status -sb` and ensure everything you want to commit is staged before reporting progress. If something should be staged, run `git add -A` and confirm staging state.
- Commit completed work in logical, scoped commits.
- Do not push automatically after committing. Push only when explicitly requested by the user.

## Session Learnings
- When adding new pages in this Vite setup, update both `src/` and `vite.config.js` (`rollupOptions.input`) so the page is built.
- Keep source/reference artifacts (meeting minutes, raw export files, root-level scratch assets) out of commits; prefer storing only production assets under `src/assets/` and ignore local root copies.
- For parallel command execution, avoid running `git commit` and `git push` at the same time; run them sequentially to prevent race conditions and lock errors.
- For image integrity-sensitive assets (e.g., QR codes), explicitly ensure no filter/tint is applied in page-specific CSS.
