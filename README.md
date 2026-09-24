# Pair Extraordinaire

Get the GitHub **Pair Extraordinaire** achievement by having a bot merge a commit that lists you as co-author.

**Get yours:** open a [pair request issue](../../issues/new?template=pair.yml) and submit it. That's it.

## How it works

1. You open an issue from the *Pair request* template.
2. A GitHub Action, running as the repo owner, makes a commit adding `pairs/<your-username>.md` with
   `Co-authored-by: you <ID+you@users.noreply.github.com>`.
3. It opens a PR with that commit, merges it, and closes your issue with a link.

The co-author is always the signed-in author of the issue, so nobody can put your name on a commit. Each user gets one pair commit.

## Setting up your own copy

1. Push this folder to a new **public** GitHub repo.
2. Create a [fine-grained personal access token](https://github.com/settings/personal-access-tokens/new)
   limited to **only this repo**, with **Contents**, **Pull requests** and **Issues** set to *Read and write*.
3. Save it as a repo secret named `PAIR_TOKEN`: `gh secret set PAIR_TOKEN -R OWNER/REPO` (paste the token when asked).
   Commits and PRs are then made as you, with each requester as co-author.
4. **Settings → General → Pull Requests:** make sure **Allow merge commits** is enabled.
5. (Optional) **Settings → Pages:** deploy from the `main` branch, `/ (root)`, to host `index.html`.
   On `*.github.io` the page detects the repo automatically; elsewhere, set `FALLBACK_REPO` in `index.html`.
6. Test it by opening a pair request from a second account or a friend's.
