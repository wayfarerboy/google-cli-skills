# 03 — Point skills at shared setup, drop no-ops, tighten configure

**What to build:** Each SKILL.md replaces its 11-line Cloud Console setup block with a context pointer to `../shared/setup.md` plus only the API-specific enable link. All three drop the `Run X --help` no-op. Configure sections tightened from 5 verbose bullets to 3 concise ones.

**Blocked by:** 01 — Extract shared Cloud Console setup

**Status:** ready-for-agent

- [ ] gccli: Cloud Console block replaced with pointer + Calendar API enable link; `--help` line removed; configure section tightened
- [ ] gmcli: Cloud Console block replaced with pointer + Gmail API enable link; `--help` line removed; configure section tightened
- [ ] gdcli: Cloud Console block replaced with pointer + Drive API enable link; `--help` line removed; configure section tightened
