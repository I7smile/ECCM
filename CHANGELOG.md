# Changelog

All notable changes to ECCM are documented here.

---

## [1.0.5] — 2026-06-20

### Added
- **Save error banner** — persistent warning when localStorage is full or disabled, with a dismiss button
- **`?` shortcut modal** — press `?` (or click the `?` button in the header) to view a full keyboard shortcut and interaction reference
- **First-run welcome card** — new users see a 3-step guide instead of a blank page
- **Toast notifications** — brief confirmations after profile switches, bulk edits, and auto-negotiated speed changes
- **Port `⋮` icon** — visible on hover; opens the speed/VLAN context menu without needing right-click
- **Bulk edit first-use hint** — a brief tooltip on first bulk mode activation
- **Cabinet section help note** — inline guide pointing users to the Edit button

### Improved
- **Port count reduction** — now shows a confirmation dialog listing exactly how many connections, aliases, and reserved ports will be deleted
- **Delete device** — confirmation now includes the number of connections that will be removed
- **Unlink** — confirmation dialog names both endpoints before disconnecting
- **Backup restore** — shows a confirmation before overwriting all profiles; improved schema validation
- **VLAN input** — inline warning when invalid values are silently dropped (range: 1–4094)
- **Print header** — now shows export date/time, device count, and connection count
- **Reserved ports in print** — RESERVED badge in the connections table; grey row background
- **Backup JSON** — no longer pretty-printed (smaller download)
- **Port accessibility** — all ports have `role="button"`, `tabindex="0"`, and Enter/Space keyboard activation
- **Settings modal** — fixed broken `aria-labelledby` reference
- **Bulk operations** — `alert()` dialogs replaced with inline inline error hints

### Fixed
- Orphaned links (referencing deleted devices) now cleaned up automatically in `normalizeState()`
- `saveStore()` previously swallowed errors silently — failures now surface a visible banner

---

## [1.0.4] — prior release

Initial public version. Core features:
- Multi-profile device and connection management
- Visual port grid with colour coding
- Cabinet / rack U visualisation
- Speed, VLAN, alias, and reserved port metadata
- Bulk port editing
- Import / export / backup / restore
- Print preview
- Dark and light themes
