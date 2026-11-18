---
name: horus-mcp
description: Use the `horus` MCP server first to discover MCP tools. Use whenever you are looking for, searching for, or trying to find an MCP tool, checking which MCP tools or servers are available, deciding which MCP tool to use, or about to conclude that no tool exists for a task.
---

# Horus MCP

1. Check whether an MCP server named `horus` is connected. If it isn't, ignore this skill and carry on as usual.
2. `horus` is a portal that uses Cloudflare's Code Mode. It doesn't load every upstream tool into context. Instead, it exposes a small **search** and **execute** interface: you write JavaScript to find tools and their schemas, then write JavaScript that calls them.
3. Search `horus` first, through its search tool (e.g. `portal_codemode_search`, which uses `codemode.tools()`). Do this before you search other servers or decide that a tool doesn't exist. `portal_list_servers` shows which upstream servers are connected.
4. Call the tools you found with its execute tool (e.g. `portal_codemode_execute`, which uses `codemode.<tool_name>(args)`).
