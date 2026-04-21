# Version History

## [1.5] - 2026-04-21
### Added
- `/bi` admin command with subcommands `reload` and `help`.
- `/bi reload` requires confirmation within 10 seconds to prevent accidental config reloads.
- `/bi help` displays all available plugin commands.

### Changed
- Default invitation and broadcast messages have been improved and switched to English for a cleaner experience.

### Fixed
- `/bi reload` now correctly reloads all configuration values, including cached messages, quick invite item properties, and cooldown settings across all executors and listeners.

---

## [1.4.1] - 2026-04-20
### Changed
- Renamed the plugin from `BedWars1058-ArenaStartMessage` to **`BedWars1058-Inviter`** to better reflect its core functionality and to avoid naming conflicts with other addons.

### Fixed
- Critical startup failure caused by incorrect plugin name references after rebranding.
- Internal package structure and import statements have been unified to ensure all components load correctly.

---

## [1.4] - 2026-04-19
### Added
- `/hh` command for server-wide announcements with configurable cooldown and message format.

---

## [1.3] - 2026-04-19
### Added
- Unified automatic invitation system with configurable interval (`auto-invite-interval`).
- New config option `enable-auto-invite` (default: false) to toggle automatic invitations.
- New message configuration `autoInviteText` and `autoInviteTulip`.

### Changed
- Merged the previous `enable-minplayers-passed` and `enable-arena-starting` toggles into a single `enable-auto-invite` option.
- Automatic invitations are now managed by a global repeating task instead of event-driven logic.

### Removed
- Deprecated `minPlayers`, `minPlayersPassedText`, `arenaStartingText`, and related options.

---

## [1.2] - 2026-04-18
### Added
- Quick invite item: a configurable bed appears in the second inventory slot during waiting/starting phases.
- Proactive state checks on world change, player join, and teleport to ensure the quick invite item is always correctly given or removed.

### Fixed
- Clicking the invitation message no longer fails with "Game not found" due to case‑sensitive arena names.
- The quick invite item is now reliably removed when the player leaves the arena or the game starts.

---

## [1.1] - 2026-04-17
### Added
- `/yq` manual invite command with cross‑world broadcasting (lobby + game world).
- Configurable toggle switches for automatic announcements.
- Cooldown system for `/yq` with customizable time and message placeholders.

---

## [1.0] - 2026-04-16
### Added
- Initial release with automatic arena start announcements for BedWars1058.
- Support for both single‑arena and BungeeCord modes.
- Clickable chat messages with hover tooltips.
- Configurable messages and sounds.
