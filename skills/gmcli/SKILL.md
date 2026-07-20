---
name: gmcli
description: Gmail CLI for searching emails, reading threads, sending messages, managing drafts, and handling labels/attachments.
---

# Gmail CLI

Command-line interface for Gmail operations.

## Installation

```bash
npm install -g @mariozechner/gmcli
```

## Setup

### Google Cloud Console (one-time)

Follow the [shared Cloud Console OAuth setup](../shared/setup.md). For step 2, use:

[Enable the Gmail API](https://console.cloud.google.com/apis/api/gmail.googleapis.com)

### Configure gmcli

First check if already configured:
```bash
gmcli accounts list
```

If no accounts, guide the user through setup:
1. Ask if they have a Google Cloud project with Gmail API enabled
2. If not, walk them through the [shared Cloud Console OAuth setup](../shared/setup.md) (use the Gmail API enable link above)
3. Have them download the OAuth credentials JSON
4. Run: `gmcli accounts credentials ~/path/to/credentials.json`
5. Run: `gmcli accounts add <email>` (use `--manual` for browserless OAuth)

## Usage

Run `gmcli --help` for full command reference.

Common operations:
- `gmcli <email> search "<query>"` - Search emails using Gmail query syntax
- `gmcli <email> thread <threadId>` - Read a thread with all messages
- `gmcli <email> send --to <emails> --subject <s> --body <b>` - Send email
- `gmcli <email> labels list` - List all labels
- `gmcli <email> drafts list` - List drafts

## Data Storage

- `~/.gmcli/credentials.json` - OAuth client credentials
- `~/.gmcli/accounts.json` - Account tokens
- `~/.gmcli/attachments/` - Downloaded attachments
