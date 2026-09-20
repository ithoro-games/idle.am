<p align="center"><img src="logo.png" alt="idle.am" width="128" /></p>

# idle.am

A cozy, competitive, real-time idle MMO. Train skills, gather resources, explore the world, and grow your character while you are away.

**[Play idle.am](https://idle.am) · [Connect an assistant](https://idle.am/connect) · [Support](https://idle.am/support)**

## Play with your assistant

This is the official public connector package for idle.am by Ithoro Games. It connects compatible assistants to the hosted idle.am MCP server. The game and server run at idle.am; this repository contains installation configuration and documentation.

- Check your character, current task, inventory, quests, and standings.
- Start and stop activities, travel, equip gear, eat food, and handle quests.
- View interactive character, task, and activity cards in clients that support MCP Apps. Other clients can use the tools through ordinary text responses.

## Connect

Add a remote MCP server using this URL:

```text
https://api.idle.am/mcp
```

Sign in to idle.am in the authorization window, check the account and character shown, and approve the requested permissions. No API key is needed.

The connector requests `play:read`, `play:act`, and `offline_access`. These allow it to read game state, perform supported gameplay actions, and stay connected between conversations. You can revoke access in idle.am Settings under Connected assistants.

The connector does not purchase anything, trade, transfer bank items, send chat messages, or change your account settings.

## Cursor

For manual installation, add this to Cursor's MCP configuration (`~/.cursor/mcp.json`, or `.cursor/mcp.json` in a project), preserving any existing servers:

```json
{
  "mcpServers": {
    "idle-am": {
      "url": "https://api.idle.am/mcp"
    }
  }
}
```

Enable the server in Cursor and complete the OAuth sign-in. This repository also includes a Cursor plugin manifest and `mcp.json` for marketplace packaging. A marketplace listing is subject to Cursor's review.

## Try asking

- "Show my idle.am character and current task."
- "What activities can I do here?"
- "Start chopping willow."
- "Show my quest progress."
- "Stop my current task."

Available actions depend on your character's level, location, equipment, and game state. Interactive cards require MCP Apps support in the client; a screenshot of a card is not interactive.

## Privacy and support

- [Privacy policy](https://idle.am/privacy)
- [Terms of service](https://idle.am/terms)
- [Support](https://idle.am/support)
- Email: support@ithoro.com

Report connector setup issues through this repository's Issues tab. Do not include access tokens, passwords, or other private account information in public issues.
