---
type: Fixed
pr: 5166
---
The secret-read guard now blocks protected file reads in shell aliases and diff.external values supplied through Git -c options, including valid global prefixes and Windows git.exe paths.
