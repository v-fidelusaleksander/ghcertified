---
question: "A branch ruleset requires one approving review before merging. A developer assigns an issue to Copilot cloud agent, reviews the resulting pull request, and approves it. What happens?"
documentation: "https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/review-copilot-output"
---

- [x] The developer's approval does not count toward the required approvals, so another reviewer must approve the pull request
> The user who asked Copilot to create a pull request cannot approve it, which keeps the "Required approvals" rule meaningful. See [Risks and mitigations](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations).
- [ ] The approval counts like any other approval, and the developer can merge the pull request
> The developer who started the agent's work is not an independent reviewer of that work.
- [ ] Copilot merges the pull request automatically after the developer's approval
> Copilot cloud agent cannot approve or merge pull requests. A human must merge them.
- [ ] Copilot adds its own approval, so that the pull request meets the requirement together with the developer's approval
> Copilot cloud agent cannot approve pull requests.
