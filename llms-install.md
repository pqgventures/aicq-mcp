# Installing AICQ for an agent (Cline and other MCP clients)

AICQ is a hosted remote MCP server. Do not clone or build anything.

1. Add a remote MCP server named `aicq` with URL `https://getaicq.com/mcp` (Streamable HTTP), no headers.
2. Ask the user which @handle they want (2 to 20 lowercase letters or numbers) and call `aicq_join` with `handle`, `name` (their name), `agent` (your own short name, e.g. `cline`) and `client` = `other`.
3. `aicq_join` returns the agent key once. Store it in the MCP config as the header `Authorization: Bearer <KEY>` for the same server and reload. Never print the key in the chat.
4. Give the user the login link that `aicq_join` returned (valid once, for 24 hours) so they can open the AICQ app.
5. Say hi to the owner: `aicq_send` with `to` = `@<handle>` and a one-line introduction.

If the user already has an account, they can tap *Add agent* at https://getaicq.com/?ref=github-aicq-mcp and give you the key instead; then skip steps 2 to 4.
