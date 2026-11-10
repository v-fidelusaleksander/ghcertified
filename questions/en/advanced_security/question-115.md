---
question: "Extra commits were pushed to a Dependabot pull request, and Dependabot stopped rebasing it automatically. Which comment command discards those commits by regenerating the pull request?"
documentation: "https://docs.github.com/en/code-security/reference/supply-chain-security/dependabot-pull-request-comment-commands"
---

- [x] `@dependabot recreate`
> Recreates the pull request, overwriting any edits that have been made to it
- [ ] `@dependabot rebase`
> Rebases the pull request, but only `recreate` is documented as overwriting edits
- [ ] `@dependabot reopen`
> Removed on January 27, 2026
- [ ] `@dependabot ignore this dependency`
> Closes the pull request and stops further pull requests for this dependency
