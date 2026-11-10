# Nekori Board Tool

A private, single-user utility for keeping one person's own Pinterest boards in order.

It is not a product, it is not published, and it has exactly one user: the account
owner. This repository exists as the public home of the app and its privacy policy,
both of which are required by the Pinterest developer platform.

## What it does

The tool runs locally on the owner's own computer as an MCP (Model Context Protocol)
server and calls the **Pinterest API v5** with the owner's own OAuth token, so the owner
can:

- list their boards and see which ones are empty, duplicated or stale
- rename a board, update its description
- merge duplicate boards
- create board sections and file pins into them
- move their own pins from one board to another
- delete empty boards and dead pins

All of the above acts on the owner's own account only. The tool cannot see, read or
touch anybody else's Pinterest content, and no Pinterest data is sent anywhere.

## What it does not do

- No Pinterest discovery, search or trend data beyond the owner's own account
- No advertising, analytics or publishing on behalf of a brand
- No multi-user access: there is no way for a second person to connect

## How it is used

```text
assistant (local)  ->  MCP server (local, stdio)  ->  Pinterest API v5  ->  owner's boards
```

Authentication is a single OAuth token issued to the owner. It is stored locally on the
owner's machine and can be revoked at any time from Pinterest account settings.

## Data

Nothing leaves the owner's computer. See [PRIVACY.md](PRIVACY.md) for the details.

## Contact

lianchihema2017@gmail.com
