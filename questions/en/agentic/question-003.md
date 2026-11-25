---
question: "The following workflow is committed to the default branch, but Copilot cloud agent ignores it and starts without the project dependencies installed. What is the cause?"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/customize-the-agent-environment"
---

```yaml
# .github/workflows/copilot-setup-steps.yml
name: "Copilot Setup Steps"
on: workflow_dispatch

jobs:
  setup:
    runs-on: ubuntu-latest
    permissions:
      contents: read
    steps:
      - uses: actions/checkout@v5
      - run: npm ci
```

- [x] The job must be named `copilot-setup-steps`, otherwise Copilot does not pick it up
> The workflow must contain a single job called `copilot-setup-steps`.
- [ ] The file must be stored in `.github/copilot/` instead of `.github/workflows/`
> The required location is `.github/workflows/copilot-setup-steps.yml`.
- [ ] The `runs-on` key must be removed because Copilot always chooses its own runner
> `runs-on` is one of the keys you can customize, for example to use larger or self-hosted runners.
- [ ] Setup steps must be declared in the custom agent profile frontmatter instead of in a workflow
> Custom agent profiles have no setup steps property. The environment is prepared by the `copilot-setup-steps.yml` workflow.
