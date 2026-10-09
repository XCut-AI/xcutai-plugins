# Installing XCut AI in Cline

XCut AI is a hosted remote MCP server. There is nothing to clone, build or install, and no API key is needed to start.

1. In Cline, open **MCP Servers → Configure** to edit `cline_mcp_settings.json`, and add:

```json
{
  "mcpServers": {
    "xcutai": {
      "type": "streamableHttp",
      "url": "https://mcp.xcut.ai/mcp",
      "disabled": false
    }
  }
}
```

2. Save. Cline connects over Streamable HTTP.
3. Hooks, playbooks and quick tools work straight away with no account.
4. Tools that use canvases, brand memory, imports or credits ask the user to sign in to XCut AI with OAuth the first time. Complete the sign-in in the browser window that opens.

XCut AI never publishes to social media.
