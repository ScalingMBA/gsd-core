---
type: Fixed
pr: 5166
---
**The secret-read guard now blocks secret reads hidden in a Git `-c` alias or `diff.external`** — `git -c alias.x='!cat .env' x` and `git -c diff.external='cat .env' diff` were allowed and printed the protected file; the configured command is now scanned like any shell script, behind any Git global option and for `git.exe` paths too.
