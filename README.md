# Nock MCP server

[![Add to Cursor](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/install-mcp?name=nock&config=eyJ1cmwiOiJodHRwczovL2FwaS51c2Vub2NrLmNvbS9tY3AifQ%3D%3D)
[![Install in VS Code](https://img.shields.io/badge/VS_Code-Install_Server-0098FF?style=flat-square&logo=visualstudiocode&logoColor=white)](https://vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%257B%2522name%2522%253A%2522nock%2522%252C%2522type%2522%253A%2522http%2522%252C%2522url%2522%253A%2522https%253A%252F%252Fapi.usenock.com%252Fmcp%2522%257D)

Nock (usenock.com) is a Brazilian B2B prospecting platform. Its remote MCP server
lets Claude, ChatGPT, Cursor, VS Code or any MCP client work on your Nock
workspace:

- search Brazilian companies by industry, size, location, CNAE and opening date,
  and the people who decide there;
- look for buying signals: companies hiring a role, raising funding, opening new
  locations, adopting a technology or in the news;
- enrich work e-mails and mobiles and keep the results in sheets;
- draft outreach campaigns. Nothing is sent until you review and activate the
  campaign in Nock.

This repository holds only the files directories and plugin marketplaces read. The
server itself runs at Nock.

## Connect

Server URL: `https://api.usenock.com/mcp` (Streamable HTTP).

You need a Nock account (500 free credits for 7 days, no card). The client opens the
Nock sign-in (OAuth) on the first call. Calls spend your workspace's credits, as in
the dashboard.

| Client | How |
|---|---|
| Claude (claude.ai, desktop, mobile) | Settings, Connectors, Add custom connector, paste the URL |
| ChatGPT | Settings, developer mode, create a connector with the URL |
| Claude Code | `claude mcp add --transport http nock https://api.usenock.com/mcp`, then `/mcp` to sign in |
| Claude Code plugin | `/plugin marketplace add nock-ltda/nock-mcp`, then `/plugin install nock@nock` |
| Cursor | the button above, or `{"mcpServers":{"nock":{"url":"https://api.usenock.com/mcp"}}}` in `mcp.json` |
| VS Code | the button above |
| Codex | `codex mcp add nock --url https://api.usenock.com/mcp` |
| Gemini CLI | `gemini extensions install https://github.com/nock-ltda/nock-mcp` |
| Windsurf | `{"mcpServers":{"nock":{"serverUrl":"https://api.usenock.com/mcp"}}}` in `mcp_config.json` |
| Zed | `"context_servers": {"nock": {"url": "https://api.usenock.com/mcp"}}` in settings |

Clients without OAuth can send a workspace API key, created on the API page of the
dashboard, as `Authorization: Bearer <key>`. Never commit the key.

Tools and docs: https://usenock.com/mcp. Privacy: https://usenock.com/privacy.
Terms: https://usenock.com/terms. Contact: contato@usenock.com.

## Files

- `server.json`: the entry in the official MCP Registry (`com.usenock/nock`).
- `.claude-plugin/marketplace.json` and `plugins/nock/`: the Claude Code plugin.
- `.cursor-plugin/marketplace.json` and `plugins/nock/`: the Cursor plugin.
- `gemini-extension.json` and `GEMINI.md`: the Gemini CLI extension.

---

## Em português

A Nock (usenock.com) é uma plataforma brasileira de prospecção B2B. O servidor MCP
dela deixa o Claude, o ChatGPT, o Cursor, o VS Code ou qualquer cliente MCP buscar
empresas e decisores, procurar sinais de compra, enriquecer contatos, guardar
resultados em planilhas e montar rascunhos de campanha no seu workspace. Nada é
enviado até você revisar e ativar a campanha na Nock.

URL do servidor: `https://api.usenock.com/mcp`. Na primeira chamada o cliente abre o
login da Nock. As chamadas usam os créditos do workspace, como no painel. Passo a
passo por cliente: https://usenock.com/mcp.
