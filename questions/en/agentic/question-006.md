---
question: "During an audit, you need to identify who is accountable for commits created by Copilot cloud agent. How are these commits attributed?"
documentation: "https://docs.github.com/en/copilot/concepts/security-governance-and-network-settings/risks-and-mitigations"
---

- [x] Copilot is the author, and the developer who assigned the issue or requested the change is a co-author
> This provides traceability back to the person who started the agent's work.
- [ ] The repository administrator is the author, because the agent acts on behalf of the repository
- [ ] `github-actions[bot]` is the author, with no reference to the developer who started the session
- [ ] The developer who assigned the issue is the only author, and Copilot is not mentioned
