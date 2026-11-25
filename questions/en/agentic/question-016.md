---
question: "A developer starts Copilot CLI with the command below. The `view`, `grep`, and `glob` tools can only read and search files. Later in the session, Copilot needs to change a file to complete the task. What happens?"
documentation: "https://docs.github.com/en/copilot/how-tos/copilot-cli/use-copilot-cli/allowing-tools"
---

```bash
copilot --available-tools='view,grep,glob' --allow-tool='write'
```

- [x] Copilot cannot change the file, because no editing tool is in the list of available tools
> `--available-tools` limits which tools Copilot can use at all. A tool that is not in this list cannot be used, even if `--allow-tool` allows it.
- [ ] Copilot changes the file without asking, because `--allow-tool='write'` allows file writes
> `--allow-tool` only removes the approval prompt for a tool. It does not make a tool available that `--available-tools` has left out.
- [ ] Copilot asks the developer for approval before it changes the file
> Copilot cannot ask for approval to use a tool that is not available in the session.
- [ ] The CLI does not start, because `--available-tools` and `--allow-tool` cannot be used together
> The two options can be combined. They control different things: which tools exist in the session, and which tools can run without approval.
