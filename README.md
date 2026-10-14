# hermes-bot-icons

Function-matched bot avatars for Hermes Agent installs (the Valicen fleet design
language: dark rounded-square, accent rim + glow, bold geometric glyph — no faces).

| Icon | Function | Accent |
|---|---|---|
| hermes | default / root profile (winged bolt) | gold |
| it | IT / ops / dev / admin | cyan |
| cmp | chief of staff / COO / CRO | amber |
| finance | finance / accounting | green |
| legal | legal / compliance | indigo |
| pmo | project / program management | blue |
| sales | sales / CRM / revenue | orange |
| marketing | marketing / brand / content | magenta |

## Install (one-liner, Linux or macOS)

    curl -fsSL https://raw.githubusercontent.com/valicen-davidsaunders/hermes-bot-icons/main/install.sh | bash

Options: `--dry-run` (preview, change nothing), `--list` (mapping only),
`HERMES_HOME=/custom/path` for non-default Hermes homes.

The installer writes `<profile>/assets/avatar.png` for the root (default) profile
and every profile under `profiles/`, mapping each profile name to a function icon
(fuzzy match; unknown names get the default hermes icon). Existing avatars are
always backed up to `avatar.png.bak-<timestamp>` first. The desktop app reads
avatars live — reopen the Bots page to refresh.

## Files
- `install.sh` — self-contained installer (icons embedded as base64, no dependencies)
- `icons/*.png` — the 8 source icons (512x512), for manual use
