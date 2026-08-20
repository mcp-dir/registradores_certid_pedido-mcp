---
name: registradores_certid_pedido-mcp
description: Skill da REST API do Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital na MCP.AI: 1 endpoint em /api/registradores_certid_pedido. Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital — REST API skill

Você tem acesso à **Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital** REST API na MCP.AI.

> Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/registradores_certid_pedido
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/registradores_certid_pedido/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"uf":"...","municipio":"...","cartorio":"...","tipo_certidao":"...","matricula":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/registradores_certid_pedido/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `registradores_certid_pedido_consultar`

Registradores (ARISP) Certidão: Novo Pedido de Certidão Digital, consulta em fonte oficial. _(POST /api/registradores_certid_pedido/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `email` | string | Não | Parâmetro de consulta "email". |
| `senha` | string | Não | Parâmetro de consulta "senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |
| `tipo_login` | string | Não | Parâmetro de consulta "tipo_login". |
| `uf` | string | Sim | Parâmetro de consulta "uf". |
| `municipio` | string | Sim | Parâmetro de consulta "municipio". |
| `cartorio` | string | Sim | Parâmetro de consulta "cartorio". |
| `tipo_certidao` | string | Sim | Parâmetro de consulta "tipo_certidao". |
| `matricula` | string | Sim | Parâmetro de consulta "matricula". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_registradores_certid_pedido` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
