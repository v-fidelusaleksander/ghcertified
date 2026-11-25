---
question: "Copilot cloud agent pushed new commits to its pull request, but none of the repository's GitHub Actions CI workflows have started. The repository uses the default settings. What explains this?"
documentation: "https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations"
---

- [x] Workflows do not run on the agent's changes until a user with write access clicks "Approve and run workflows"
> Workflows can have access to secrets and privileged tokens, so a human first reviews the agent's code before it runs in CI. See also [Review output from Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/review-copilot-output).
- [ ] Workflows never run on pull requests from the cloud agent, so CI must be started manually with `workflow_dispatch`
> Workflows do run once they are approved, and the repository can also be configured to run them automatically.
- [ ] The workflows already ran with a read-only `GITHUB_TOKEN` and without secrets, like pull requests from forks
> By default, the workflows do not run at all until they are approved.
- [ ] The cloud agent approves the workflow runs itself after its built-in security validation passes
> The cloud agent cannot approve its own workflow runs. A user with write access must approve them.
