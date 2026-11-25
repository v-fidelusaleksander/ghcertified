---
question: "A `schema-migrator` custom agent should only run when another custom agent delegates work to it. Developers must not be able to select it manually. Which frontmatter setting do you use?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration"
---

- [x] `user-invocable: false`
> When `user-invocable` is `false`, the agent cannot be selected manually and can only be accessed programmatically.
- [ ] `disable-model-invocation: true`
> This does the opposite: it stops Copilot from choosing the agent automatically, so the agent must be selected manually.
- [ ] `infer: false`
> `infer` is retired. `infer: false` is equivalent to `disable-model-invocation: true`.
- [ ] `target: github-copilot`
> `target` limits the environment (`vscode` or `github-copilot`) where the agent is available, not who can invoke it.
