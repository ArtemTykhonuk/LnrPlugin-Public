# Lnr — Changelog

All notable changes to the Lnr plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com), and this project adheres to [Semantic Versioning](https://semver.org).

## [1.2.0] - 2026-05-19

### Added
- **Inbox / Notifications:** New "Inbox" tab in the Lnr Tool Window mirrors Linear's Inbox, letting you stay updated without leaving the IDE.
  - Paginated list of notifications with relative timestamps ("5m ago", "2h ago", etc.)
  - Bold text + unread dot for unread notifications; per-type icons for visual distinction
  - Click a notification to open the related issue in the Detail Panel
  - Right-click context menu: "Mark as read/unread", "Archive"
  - Header actions: "Mark all as read" and "Archive all" with optimistic UI updates
  - Scroll-to-bottom pagination loads more notifications automatically
- **Status Bar Unread Badge:** The Lnr status bar widget now displays `Lnr [N]` (capped at `[99+]`) when unread notifications are present; clicking the widget focuses the Inbox tab.
- **Background Notification Polling:** Notifications are fetched on startup and refreshed every 60 seconds independently of the issue polling cycle.
- **Emoji Reactions on Comments:** Each comment card now shows aggregated reaction pills (one per emoji, with reactor count and a tooltip listing names) and an Add-reaction button that opens a full Unicode emoji picker. Clicking your own reaction toggles it off; clicking someone else's emoji adds your reaction.
- **Full Unicode Emoji Picker:** The reaction picker ships with a curated Unicode catalog (~600 emojis across 8 categories — Smileys, Hands, Hearts, Symbols, Objects, Nature, Food, Activities), a live **search field** that filters by name or shortcode (e.g. `heart` → ❤️ 🧡 💛), and a **Recently used** strip that persists across IDE restarts.
- **Comment Thread Resolution:** Replies in a comment thread can now be marked as the thread's *resolution*. A small `✓ Mark as resolution` button sits in the reply footer, and every reply card also carries a `⋮` menu with the same action plus `Reopen thread` when that reply is the current resolver. The resolving reply renders a green **Resolution** badge above its body.
- **Attachments Management:** A new **Attachments** section in the Issue Detail Panel lets you work with files without leaving the IDE.
  - View existing attachments with MIME-typed icons (image, text, archive, JSON, generic), title, human-readable size, and uploader name
  - Left-click an attachment to open it in the browser; right-click for "Open in Browser" / "Delete"
  - Upload a new file via the toolbar **Upload** button (single-file chooser) or by dragging a file from the OS onto the panel
  - Indeterminate progress bar is shown while the file streams to Linear; the section refreshes automatically on success
  - Pre-flight checks reject multi-file drops and files larger than Linear's 25 MB limit with a clear notification

### Deferred from v1.2.0
- **Multi-workspace Support** — moved to **v1.3.0**.
- **Saved Filters & Custom Views** — moved to **v1.2.1**.

## [1.1.0] - 2026-04-07

### Added
- **Sub-issues support:** Full hierarchical display in list and Kanban views, parent navigation, and creation with autocomplete.
- **Due Dates:** View and edit due dates on issues with color-coded overdue indicators.
- **Threaded Comment Replies:** View nested comment threads and reply directly within the IDE.
- **Issue Relations:** View "Blocks", "Blocked by", and "Related" issue dependencies in the detail panel.
- **Issue Estimates:** Support for team-specific estimation scales (Fibonacci, Exponential, T-Shirt, etc.) in view and edit modes.

### Improved
- **Auto-connect on Startup:** Plugin now automatically restores credentials and connects on IDE startup.

## [1.0.2] - 2026-04-01

### Fixed
- Fixed user name not being remembered after IDE restart, causing branch names to use "user/" instead of the actual username
- Fixed duplicate "Loading" indicators appearing at the bottom of Issues and Kanban tabs during refresh
- Fixed empty space appearing in the issue detail view after editing labels

## [1.0.1] - 2026-03-30

### Fixed
- Improved compatibility with JetBrains IDEs version 2024.1 and newer
- Resolved an issue where opening plugin settings could cause a brief UI freeze

### Improved
- Enhanced plugin listing and discoverability on JetBrains Marketplace

## [1.0.0] - 2026-03-25

### Added

#### Issue Management
- Browse, search, and filter Linear issues directly from the IDE
- "All Teams" mode — view and manage issues across all your Linear teams in one place
- Filter by team, workflow state, assignee, and priority
- Create issues with full field support: title, description, team, state, priority, assignee, project, cycle, and labels
- Edit issues inline — modify all fields in the detail panel without opening Linear
- View and post comments on issues (Cmd+Enter / Ctrl+Enter to send)
- Delete issues from the detail panel
- Issue detail panel with full metadata, labels, and comments

#### Kanban Board
- Board view — columns grouped by workflow state with color-coded status headers
- List view — collapsible grouped rows in Linear's style
- Toggle between Board and List views — preference is remembered across sessions
- Drag-and-drop to change issue status (works on columns, row headers, and individual rows)
- Multi-team support with merged status columns in "All Teams" mode

#### AI-Powered Description Generation
- ✨ Generate structured issue descriptions from a title and optional context
- Dual AI provider support:
  - **JetBrains AI Assistant** — zero configuration, uses your existing AI Assistant setup
  - **OpenAI-compatible (BYOK)** — bring your own API key (GPT-4o, GPT-4o-mini, Claude, Ollama, etc.)
- Available in both Create Issue dialog and Edit Issue panel
- AI provider selection and configuration in Settings → Tools → Lnr
- Model dropdown with 9 presets + custom model name support

#### Issue Templates
- Save frequently used issue configurations as reusable local templates
- Quick-apply templates from a dropdown in the Create Issue dialog
- Templates store title, description, team, state, priority, and assignee

#### Git Integration
- Create and auto-checkout Git branches named after the selected issue (e.g. `feature/BE-123-issue-title`)
- Copy formatted branch name to clipboard
- Auto-detect Linear issue identifiers from current branch name
- Smart commit message prefixing with the current issue identifier

#### Cycles & Workflow
- Cycle tracking with progress indicators for active and completed cycles
- Team selector in the Cycles tab to switch between teams
- Auto-refresh with configurable polling interval and exponential backoff on errors
- Status bar widget showing Linear connection status
- Balloon notifications for errors and important events
- Open any issue in the Linear web app with one click

#### Keyboard Shortcuts
- `C` — Create Issue
- `Ctrl+Shift+B` / `Cmd+Shift+B` — Create Branch
- `Ctrl+Shift+C` / `Cmd+Shift+C` — Copy Branch Name
- `O` — Open in Browser
- `R` — Refresh
- `Esc` — Close detail panel

#### Cross-IDE Support
- Compatible with all JetBrains IDEs: IntelliJ IDEA, WebStorm, PyCharm, Rider, GoLand, PhpStorm, CLion, RubyMine, DataGrip, and more
- Native platform icons (`AllIcons`) for toolbar buttons with automatic light/dark theme support
- HiDPI-scaled UI via `JBUI.scale()` for retina displays
- Dark theme icon variant (`pluginIcon_dark.svg`)

#### Settings & Authentication
- API key authentication via JetBrains PasswordSafe (secure credential storage)
- Test Connection button to verify API key before saving
- Configurable auto-refresh interval
- AI provider configuration (JetBrains AI / OpenAI-compatible / Disabled)
