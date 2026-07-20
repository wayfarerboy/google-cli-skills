# 01 — Extract shared Cloud Console setup

**What to build:** A single `skills/shared/setup.md` containing the 5-step Google Cloud Console OAuth setup that's currently duplicated across all three skills. Each step gets a parameterized slot for the API-specific enable link so gccli/gmcli/gdcli can point at the shared file and supply only their API.

**Blocked by:** None — can start immediately.

**Status:** ready-for-agent

- [ ] `skills/shared/setup.md` exists with the full Cloud Console OAuth flow
- [ ] Each tool-specific enable link is a parameter the calling skill supplies
- [ ] All three SKILL.md files still reference the correct API enable step
