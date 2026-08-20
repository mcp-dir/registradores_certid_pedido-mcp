# Instalação detalhada

Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_registradores_certid_pedido`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_registradores_certid_pedido` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_registradores_certid_pedido` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_registradores_certid_pedido` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.registradores_certid_pedido` (ou `servers.registradores_certid_pedido` no VS Code) do config do cliente e reinicie.
