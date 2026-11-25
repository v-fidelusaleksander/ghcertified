---
question: "A team wants to make sure that pull requests from Copilot cloud agent cannot be merged when they introduce a code scanning alert with a security severity of high or critical. What should they configure?"
documentation: "https://docs.github.com/en/code-security/code-scanning/managing-your-code-scanning-configuration/set-code-scanning-merge-protection"
---

- [x] A branch ruleset with the "Require code scanning results" rule, using CodeQL as the required tool and the security alerts threshold set to "High or higher"
> The cloud agent is subject to the branch protections and required checks of the repository. See [Risks and mitigations](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations).
- [ ] The same ruleset, but with the security alerts threshold set to "Critical"
> This only blocks critical alerts. High severity alerts can still be merged.
- [ ] Nothing extra, because the cloud agent's built-in CodeQL validation already blocks the merge
> The built-in validation lets the agent try to fix issues before it finishes its work, but it is not a merge gate.
- [ ] An instruction in `.github/copilot-instructions.md` that forbids introducing high severity vulnerabilities
> Custom instructions guide the agent, but they cannot prevent a pull request from being merged.
