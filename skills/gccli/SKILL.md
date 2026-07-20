---
name: gccli
description: Use when the user wants to list calendars, view/create/update events, or check availability
---

# Google Calendar CLI

Command-line interface for Google Calendar operations.

## Installation

```bash
npm install -g @mariozechner/gccli
```

## Setup

### Google Cloud Console (one-time)

Follow the [shared Cloud Console OAuth setup](../shared/setup.md). For step 2, use:

[Enable the Google Calendar API](https://console.cloud.google.com/apis/api/calendar-json.googleapis.com)

### Configure gccli

First check if already configured:
```bash
gccli accounts list
```

If no accounts, guide the user through setup:
1. Get credentials JSON from the Cloud Console OAuth setup above
2. Run: `gccli accounts credentials ~/path/to/credentials.json`
3. Run: `gccli accounts add <email>` (use `--manual` for browserless OAuth)

## Usage

Common operations:
- `gccli <email> calendars` - List all calendars
- `gccli <email> events <calendarId> [--from <dt>] [--to <dt>]` - List events
- `gccli <email> event <calendarId> <eventId>` - Get event details
- `gccli <email> create <calendarId> --summary <s> --start <dt> --end <dt>` - Create event
- `gccli <email> freebusy <calendarIds> --from <dt> --to <dt>` - Check availability

Use `primary` as calendarId for the main calendar.

## Date/Time Format

- Timed events: `YYYY-MM-DDTHH:MM:SSZ` (UTC) or `YYYY-MM-DDTHH:MM:SS` (local)
- All-day events: `YYYY-MM-DD` with `--all-day` flag

## Data Storage

- `~/.gccli/credentials.json` - OAuth client credentials
- `~/.gccli/accounts.json` - Account tokens
