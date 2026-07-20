---
name: gmcli
description: Use when the user wants to search emails, read threads, send messages, manage drafts, handle labels or attachments
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
1. Get credentials JSON from the Cloud Console OAuth setup above
2. Run: `gmcli accounts credentials ~/path/to/credentials.json`
3. Run: `gmcli accounts add <email>` (use `--manual` for browserless OAuth)

## Usage

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
