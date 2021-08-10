# Fourmolu — Developer notes

## Merging upstream

Fourmolu aims to continue merging upstream changes in Ormolu. Every so often, a PR should be made that takes upstream Ormolu changes and merges them into Fourmolu. This is the workflow to follow:

1. `cd` into your local copy of the Fourmolu repository
1. Add Ormolu as an upstream remote: `git remote add ormolu git@github.com:tweag/ormolu`
1. Check out a new branch: `git switch -c merge-ormolu`
1. Merge in Ormolu changes: `git merge ormolu/master`
1. (Recommended) Switch to diff3 conflicts: `git checkout --conflict=diff3`. This provides more context that might be helpful for resolving conflicts. See [docs](https://git-scm.com/book/en/v2/Git-Tools-Advanced-Merging#_checking_out_conflicts).
1. Resolve conflicts + finish merge: `git merge --continue`
