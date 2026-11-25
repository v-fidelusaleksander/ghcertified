---
question: "A team copies the custom agent profile below from their VS Code setup to `.github/agents/accessibility-auditor.agent.md`. What happens to the `handoffs` property when the agent is used by Copilot cloud agent on GitHub.com?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

```yaml
---
name: accessibility-auditor
description: Audits UI components for accessibility issues
tools: ["read", "search"]
handoffs:
  - label: Fix the issues
    agent: ui-fixer
    prompt: Fix the accessibility issues listed above.
---
```

- [x] The property is ignored, and the rest of the profile is used as usual
> `handoffs` and `argument-hint` are supported in VS Code and other IDEs, but they are ignored by Copilot in the cloud on GitHub.com.
- [ ] The cloud agent automatically starts a new session with the `ui-fixer` agent when the audit is finished
> Handoffs are not supported on GitHub.com, so no follow-up agent is started.
- [ ] The profile fails validation, and the agent is not available on GitHub.com
> Unsupported IDE-only properties are ignored to keep profiles compatible across environments.
- [ ] The cloud agent shows a button in the pull request to switch to the `ui-fixer` agent
> Handoff buttons are a feature of the chat experience in VS Code, not of the cloud agent on GitHub.com.
