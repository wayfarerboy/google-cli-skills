# Google CLI Skills

Pi coding agent skills for Google CLI tools by [@mariozechner](https://github.com/mariozechner).

## Skills

| Skill | Description |
|-------|-------------|
| [gmcli](./skills/gmcli/SKILL.md) | Gmail CLI — search emails, read threads, send messages, manage drafts, handle labels and attachments |
| [gdcli](./skills/gdcli/SKILL.md) | Google Drive CLI — list, search, upload, download, or share Drive files and folders |
| [gccli](./skills/gccli/SKILL.md) | Google Calendar CLI — list calendars, view, create, update events, or check availability |

## Setup

One-time OAuth setup is required — follow the [shared Cloud Console OAuth setup](./skills/shared/setup.md). Each skill's `SKILL.md` includes its own install command and the specific API enable link for step 2.

## Install as Pi Package

```bash
pi install git:github.com/wayfarerboy/google-cli-skills
```
