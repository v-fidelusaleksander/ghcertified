---
question: "A developer adds a remote MCP server to the repository's MCP configuration for Copilot cloud agent. The server only supports OAuth for authentication. What is the result?"
documentation: "https://docs.github.com/en/copilot/how-tos/use-copilot-agents/cloud-agent/extend-cloud-agent-with-mcp"
---

- [x] This is not supported, because the cloud agent does not support remote MCP servers that use OAuth
> Remote servers configured for the cloud agent can authenticate with static `headers`, such as an API key stored in a secret.
- [ ] The cloud agent pauses the session and asks the developer who assigned the task to complete the OAuth sign-in
> The cloud agent runs non-interactively and does not support OAuth-based remote servers.
- [ ] The server works if it is defined in the `mcp-servers` property of a custom agent profile instead
> The same limitation applies to MCP servers defined in custom agent profiles.
- [ ] The cloud agent reuses the OAuth session that the developer created for the server in VS Code
> Sessions from the developer's IDE are not shared with the cloud agent.
