---
question: "A developer adds a remote MCP server to the repository's MCP configuration for Copilot cloud agent. The server only supports OAuth for authentication. What is the result?"
documentation: "https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/configure-mcp-servers"
---

- [x] This is not supported, because the cloud agent does not support remote MCP servers that use OAuth
> Remote servers configured for the cloud agent can authenticate with `headers` that reference an Agents secret, such as `$COPILOT_MCP_API_KEY`.
- [ ] The cloud agent pauses the session and asks the developer who assigned the task to complete the OAuth sign-in
> The cloud agent runs non-interactively and does not support OAuth-based remote servers.
- [ ] The server works if it is defined in the `mcp-servers` property of a custom agent profile instead
> The limitation applies to MCP servers configured in repository settings and in custom agent profiles.
- [ ] The cloud agent reuses the OAuth session that the developer created for the server in VS Code
> Sessions from the developer's IDE are not shared with the cloud agent.
