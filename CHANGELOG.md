# Lnr — Changelog

All notable changes to the Lnr plugin will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com), and this project adheres to [Semantic Versioning](https://semver.org).

## [1.0.0] - 2026-03-23

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
