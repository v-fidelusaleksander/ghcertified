---
question: "You are designing a custom agent profile for a reviewer agent that may only read and search code, and may only call the `get_ticket` tool of the repository-configured `tracker` MCP server. Which `tools` value achieves this?"
documentation: "https://docs.github.com/en/copilot/reference/custom-agents-configuration#tools"
---

- [x] `tools: ["read", "search", "get_ticket"]`
> Tool aliases enable built-in tools, and listing an MCP tool by name enables only that tool. You can also prefix the tool with the server name, such as `tracker/get_ticket`, which is useful when several MCP servers provide a tool with the same name.
- [ ] `tools: ["read", "search", "tracker/*"]`
> `tracker/*` enables all tools from the `tracker` server, not only `get_ticket`.
- [ ] Omit the `tools` property and list the allowed tools in the prompt body
> Omitting `tools` enables all available tools. Instructions in the prompt are not an enforced permission boundary.
- [ ] `tools: []` combined with an `mcp-servers` entry for `tracker` that only lists `get_ticket`
> An empty list disables all tools for the agent, including MCP tools.
