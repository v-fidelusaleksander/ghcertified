---
question: "A step in the `copilot-setup-steps` job of a repository exits with a non-zero exit code. How does Copilot cloud agent behave?"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/customize-the-agent-environment"
---

- [x] It skips the remaining setup steps and starts working with the current state of the development environment
> A failing setup step does not abort the session, so check the session logs when the agent behaves as if a tool or dependency is missing.
- [ ] It aborts the session and comments on the issue that the environment could not be prepared
- [ ] It retries the failed step up to three times before aborting the session
- [ ] It ignores the failure and continues running the remaining setup steps
