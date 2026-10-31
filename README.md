# Xevol MCP server

Connect Claude, ChatGPT, Codex, Claude Code or pi to one Xevol Workspace. Your agent reads and drafts there. A person approves, sends, publishes and deletes.

This repository holds documentation only. The server runs at xevol.com; its source is private.

## Connect

Coding agents (`claude`, `codex` or `pi`):

```sh
npx xevol connect claude
```

The command shows a sign-in code. Approve it in any browser and pick a Workspace. `npx xevol connect other` prints the URL and header for any other MCP client.

Apps that accept an MCP server URL, such as ChatGPT:

```text
https://xevol.com/api/mcp
```

Claude, which leaves out AI picture, video and voice tools:

```text
https://xevol.com/api/mcp/listed
```

## How it works

- **Sign-in:** OAuth 2.1 with PKCE and dynamic client registration, over streamable HTTP.
- **Scope:** one Workspace per connection, fixed when you approve. The agent acts with your rights there.
- **Paid work:** anything the agent starts uses that Workspace's credits.
- **Lifetime:** a connection lasts six months, then you sign in again.
- **Control:** Settings lists each connected agent. Remove one and its token stops working.

You need a Xevol account. See [pricing](https://xevol.com/pricing).

## Links

- [Connector guide](https://xevol.com/mcp)
- [MCP Registry entry](https://registry.modelcontextprotocol.io/v0/servers?search=com.xevol/xevol): `com.xevol/xevol`
- [`xevol` on npm](https://www.npmjs.com/package/xevol)
- Support: support@xevol.com
