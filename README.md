# OpenCode-oAuth

## Instructions

### 1. Clone this branch

```bash
git clone -b mcp-auth-workaround https://github.com/connorads/opencode.git opencode-mcp-auth
cd opencode-mcp-auth
```

### 2. Install dependencies

```bash
bun install
```

### 3. Configure your MCP server

If not already done, add the remote MCP server to your `~/.config/opencode/opencode.json`:

```json
{
  "mcp": {
    "your-mcp-server": {
      "url": "https://mcp.example.com/mcp"
    }
  }
}
```

Replace `your-mcp-server` with whatever name you want, and update the URL accordingly.

### 4. Authenticate

```bash
bun dev mcp auth your-mcp-server
```

Replace `your-mcp-server` with the name you used in step 3.

This will open your browser to complete the OAuth flow.

### 5. Done!

The auth tokens are stored in `~/.opencode/mcp-auth.json` or `~/.local/share/opencode/mcp-auth.json` and will work with your regular OpenCode installation. You can now use the MCP server with vanilla OpenCode - you don't need this branch anymore.
