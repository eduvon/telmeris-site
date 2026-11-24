# Telmeris website

## Preview locally

From the repository root, run `python3 -m http.server 8000`, then open `http://localhost:8000/`. The blog page is at `http://localhost:8000/blog/`, the featured article is at `http://localhost:8000/blog/real-value-of-ai/`, and the partners page is at `http://localhost:8000/partners/`. Stop the server with `Ctrl+C`.

Do not open the `blog/` or `partners/` folders directly from Finder or with a `file://` URL. Browsers show a directory listing for local folders; the local server resolves each clean route to its `index.html` page.

## Save future changes

Work on a feature branch, review `git status` and `git diff`, then add only the intended files and commit with a clear message:

```sh
git switch -c feature/short-description
git status
git diff
git add path/to/changed-file
git commit -m "Describe the change"
```

Keep credentials, local environment files, dependencies, and generated build output out of commits. This site is currently a small static HTML site; do not add generated files unless the project needs them.

## Roll back

To undo a change while preserving the history, use `git revert <commit>` on the branch containing that change, then review and commit the revert. To return to an earlier committed state for local inspection, use `git switch --detach <commit>`; switch back to your branch when finished. Avoid `git reset --hard` unless you intentionally want to discard local work.
