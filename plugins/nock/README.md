# Nock B2B Prospecting plugin for Claude Code

Connects Claude Code to the Nock MCP server at `https://api.usenock.com/mcp`.
Nock (usenock.com) is a Brazilian B2B prospecting platform: with this plugin Claude
can search Brazilian companies and the people who decide there, follow buying
signals, enrich contacts, keep results in sheets and draft outreach campaigns in
your Nock workspace. Nothing is sent until you review and activate a campaign in
Nock.

## Install

```
/plugin marketplace add nock-ltda/nock-mcp
/plugin install nock-prospecting@nock
```

On Claude Code 2.1.275 or later, one step also works:

```
/plugin install nock-prospecting --marketplace nock-ltda/nock-mcp
```

After installing, run `/mcp` in Claude Code and sign in with your Nock account.
Calls use your workspace's credits, as in the dashboard. Setup for other clients:
https://usenock.com/mcp

## Links

- Docs: https://usenock.com/mcp
- Privacy: https://usenock.com/privacy
- Terms: https://usenock.com/terms
- Support: https://usenock.com/contact (or e-mail contato@usenock.com)
