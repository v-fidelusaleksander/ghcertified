---
question: "Copilot cloud agent uses the custom agent `api-reviewer` and has opened a pull request. While that pull request is still open, a developer commits a change to the agent's profile file, `.github/agents/api-reviewer.agent.md`, on the default branch. Which statements are true?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] Follow-up work in the open pull request, such as responding to review comments, uses the version of `api-reviewer.agent.md` that created the pull request
> Interactions within a pull request use the same version of the custom agent for consistency.
- [x] If a developer then assigns another issue to Copilot with the `api-reviewer` agent selected, that new session uses the updated `api-reviewer.agent.md`
> A new session uses the latest version of the profile file for that repository and branch, here the default branch.
- [ ] The open pull request switches to the updated `api-reviewer.agent.md` with the next `@copilot` comment
> The version is not switched in the middle of a pull request, so changes to the file cannot alter work that is already in progress.
- [ ] The agent session for the open pull request fails because `api-reviewer.agent.md` changed
> Work in the open pull request continues with the version it started with.
- [ ] The change only takes effect after you increase a `version` property in the frontmatter of `api-reviewer.agent.md`
> Custom agent versions are based on the Git commit SHAs of the profile file. There is no `version` property.
