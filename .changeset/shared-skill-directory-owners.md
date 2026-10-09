---
"openwiki": patch
---

Codex, IBM Bob, and project-scope Antigravity all install the OpenWiki
skill to `.agents/skills/openwiki`. Let those hosts co-own the shared skill
directory so installing one no longer marks the others as modified or requires
`--force`.

Record each owning host with its own MCP command while preserving the existing
receipt shape for single-host installations. Installing another host now joins
the existing ownership, uninstalling one host removes only its MCP entry and
ownership, and the shared directory is removed with its last owner. Receipt
updates are written atomically.
