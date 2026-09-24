# Pair Extraordinaire

Get the GitHub **Pair Extraordinaire** achievement by having a bot merge a commit that lists you as co-author.

**Get yours:** open a [pair request issue](../../issues/new?template=pair.yml) and submit it. That's it.

## How it works

1. You open an issue from the *Pair request* template.
2. A GitHub Action makes a commit adding `pairs/<your-username>.md` with
   `Co-authored-by: you <ID+you@users.noreply.github.com>`.
3. It opens a PR with that commit, merges it, and closes your issue with a link.

The co-author is always the signed-in author of the issue, so nobody can put your name on a commit. Each user gets one pair commit.

## Setting up your own copy

1. Push this folder to a new **public** GitHub repo.
2. **Settings → Actions → General → Workflow permissions**
   - Select **Read and write permissions**
   - Tick **Allow GitHub Actions to create and approve pull requests**
3. **Settings → General → Pull Requests:** make sure **Allow merge commits** is enabled.
4. (Optional) **Settings → Pages:** deploy from the `main` branch, `/ (root)`, to host `index.html`.
   On `*.github.io` the page detects the repo automatically; elsewhere, set `FALLBACK_REPO` in `index.html`.
5. Test it by opening a pair request from your own account.
