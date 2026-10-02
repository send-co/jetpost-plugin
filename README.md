# Jetpost plugin

Build on each other's ideas. Tell your agent "make a note." Your team, and
their agents, can pick it up from there.

Jetpost is an inbox of notes for people and their agents. A note you write in
Claude, ChatGPT, Cursor or any other AI lands in your teammates' inboxes. They
can read it, comment on a passage, or have their own agent edit it or add to
it. Every change an agent makes is marked as the agent's.

This plugin bundles the hosted Jetpost MCP server and a skill that helps you
pick who to ask for feedback once a note is written.

## Install

**Claude (Claude Code and Cowork)**

```
/plugin marketplace add send-co/jetpost-plugin
/plugin install jetpost@jetpost
```

**Cursor**

Install Jetpost from the Cursor marketplace.

**Gemini CLI**

```
gemini extensions install https://github.com/send-co/jetpost-plugin
```

Or point any MCP client at the server directly:

```
https://www.jetpost.com/mcp
```

## Authentication

Jetpost uses OAuth 2.1 with PKCE. There's no API key to copy.

- Endpoint: `https://www.jetpost.com/mcp` (Streamable HTTP)
- The first time a tool runs, your client opens a browser so you can sign in
- Your client holds the tokens. This repository never sees them.

## What's included

| Component | |
|---|---|
| MCP server | `.mcp.json`: the hosted Jetpost server |
| Skill | `jetpost-share-for-feedback`: suggests 3–5 people to ask for feedback on a note, then helps send it |

## Tools

| Tool | What it does |
|---|---|
| `create_note` | Write a note and share it with teammates, or keep it to yourself |
| `search_notes` | Find notes you wrote or received |
| `get_note` | Read a note and its comment threads |
| `edit_note` | Replace part of a note |
| `append_to_note` | Add to the end of a note |
| `add_comment` | Comment on a note or a passage, or reply in a thread |
| `share_note` | Add people to a note and email them when it's ready |
| `list_members` | List the people in your workspace |
| `upload_image` | Add an image to a note |

## What it sends and fetches

The plugin talks only to `https://www.jetpost.com`. It sends what you ask your
agent to write (note text, comments, images and the people to share with) and
fetches the notes you can read. It sends nothing to anyone else.

Jetpost emails a note's recipients only when you say the note is ready to go
out. The feedback skill may look at the chat history, Slack, calendar or email
your agent can already access, but only to work out who you talk to most. It
doesn't quote or store those messages.

## Links

- [jetpost.com](https://www.jetpost.com/welcome)
- [Privacy policy](https://www.jetpost.com/privacy)
- [Terms of service](https://www.jetpost.com/terms)
- Support: [support@jetpost.com](mailto:support@jetpost.com) or [open an issue](https://github.com/send-co/jetpost-plugin/issues)

## License

MIT. See [LICENSE](LICENSE).
