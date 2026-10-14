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

The repo is **private** (Valicen fleet assets), so clone with your existing
GitHub git credentials — the same way you clone any of the cenlogic/valicen repos:

    git clone --depth 1 https://github.com/valicen-davidsaunders/hermes-bot-icons /tmp/hbi && bash /tmp/hbi/install.sh

On a machine with the `gh` CLI authenticated, equivalently:

    gh repo clone valicen-davidsaunders/hermes-bot-icons /tmp/hbi && bash /tmp/hbi/install.sh

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
