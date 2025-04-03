#   MCP Server Setup Cheatsheet
- https://modelcontextprotocol.io/tutorials/building-mcp-with-llms

## Preparing the Documentation

Before starting, gather the necessary documentation to help Claude understand MCP:

1. Visit [MCP Full Documentation](https://modelcontextprotocol.io/llms-full.txt) and copy the full documentation text.
2. Navigate to either the MCP **TypeScript SDK** or **Python SDK** repository.
3. Copy the README files and other relevant documentation.
4. Paste these documents into your conversation with Claude.

---

## Describing Your Server

Once you’ve provided the documentation, clearly describe to Claude what kind of server you want to build. Be specific about:

- **What resources** your server will expose.
- **What tools** it will provide.
- **Any prompts** it should offer.
- **What external systems** it needs to interact with.

### Example Prompt:

```plaintext
Build an MCP server that:
- Connects to my company's PostgreSQL database
- Exposes table schemas as resources
- Provides tools for running read-only SQL queries
- Includes prompts for common data analysis tasks
```
