# `@agentchain/mcp-oracle` (docs scaffold)

This package is a **demo / audit scaffold**: a stdio MCP server that exposes a small, simulated view of the public OpenAPI surface. It is **not** the **Humbleaf MCP (authority)** endpoint.

| | Docs MCP oracle (this folder) | Humbleaf MCP (authority) |
|--|--------------------------------|---------------------------|
| Transport | stdio | HTTPS `POST /mcp` on the API gateway |
| Auth | None | `Authorization: Bearer acmd_…` (agent mandate) |
| Side effects | None (simulated fetch) | Guarded routes (email reply under HMCP-1) |
| Docs | This README | `apps/docs/agent-operators/humbleaf-mcp-authority.mdx` |

Do not configure Cursor or Grok to treat this server as the authority runtime. Use the gateway `/mcp` endpoint and operator-issued mandates instead.

Build: `pnpm --filter @agentchain/mcp-oracle build` (TypeScript compile in this package only).
