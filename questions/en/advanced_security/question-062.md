---
question: "What is the effect of adding the `paths-ignore` keyword to your code scanning GitHub Actions workflow?"
documentation: "https://docs.github.com/en/code-security/reference/code-scanning/workflow-configuration-options#avoiding-unnecessary-scans-of-pull-requests"
---

```yaml
.github/workflows/codeql-analysis.yml

on:
  pull_request:
    branches: [main]
    paths-ignore:
      - '**/*.md'
      - '**/*.txt'

```
- [x] Avoiding unnecessary scans when files that are not relevant to the analysis are changed.
> `paths-ignore` at the workflow trigger-level controls whether the workflow runs. If a PR touches only ignored files, the workflow doesn't run.
- [ ] It tells CodeQL to omit all `*.txt` and `*.md` files from the analysis.
> To control what files are analyzed when the workflow runs, define `paths-ignore` either in a CodeQL configuration file passed in the `config-file:` input of the `init` step, or as YAML string passed in the `config:` input of the `init` step. [Read more on specifying directories to scan in workflow configuration options](https://docs.github.com/en/enterprise-cloud@latest/code-security/reference/code-scanning/workflow-configuration-options#specifying-directories-to-scan). 
- [ ] Preventing the CodeQL analysis from running on pull requests that change files with the specified extensions.
- [ ] Pull request checks will ignore any CodeQL vulnerabilities that are found in `*.txt` and `*.md` files.
