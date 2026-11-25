---
question: "A custom agent named `docs-writer` is defined at the repository level and at the organization level. Which definition does Copilot use when working in that repository?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] The repository-level definition, because the lowest level configuration overrides higher levels
> A repository-level agent overrides an organization-level agent, which in turn overrides an enterprise-level agent.
- [ ] The organization-level definition, because organization settings always take precedence over repository settings
- [ ] Both definitions are merged, and the organization profile wins for conflicting properties
- [ ] Neither, because duplicate custom agent names cause a validation error
