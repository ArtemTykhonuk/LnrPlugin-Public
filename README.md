<p align="center">
  <img src="assets/lnr-icon.svg" alt="Lnr Logo" width="80" height="80">
</p>

<h1 align="center">Lnr — Linear Integration for JetBrains IDEs</h1>

<p align="center">
  The most complete <a href="https://linear.app">Linear.app</a> integration for JetBrains IDEs.<br>
  Manage issues, drag-and-drop on a Kanban board, create Git branches, generate descriptions with AI — without leaving your editor.
</p>

<p align="center">
  <a href="https://plugins.jetbrains.com/plugin/30909-lnr"><img src="https://img.shields.io/jetbrains/plugin/v/30909-lnr.svg?label=Marketplace&color=6C63FF" alt="JetBrains Marketplace"></a>
  <a href="https://plugins.jetbrains.com/plugin/30909-lnr"><img src="https://img.shields.io/jetbrains/plugin/d/30909-lnr.svg?color=6C63FF" alt="Downloads"></a>
  <a href="https://plugins.jetbrains.com/plugin/30909-lnr/reviews"><img src="https://img.shields.io/jetbrains/plugin/r/rating/30909-lnr?color=6C63FF" alt="Rating"></a>
</p>

---

## 🎉 What's new in 1.2.0

- **Inbox** — A dedicated Inbox tab mirrors Linear's notifications, with an unread badge on the status bar, archive/unarchive, and background polling every 60 seconds.
- **Emoji Reactions** — React to comments with a full Unicode picker featuring live search and a "Recently used" strip. Reaction pills are grouped per emoji with reactor tooltips.
- **Attachments** — View, open, and delete attachments on issues, or upload new files via picker or drag-and-drop (25 MB per file).
- **Comment Thread Resolution** — Mark a specific reply as the thread's resolution; the resolving reply gets a green **Resolution** badge and can be reopened from a `⋮` menu.

See [CHANGELOG.md](CHANGELOG.md#120---2026-05-19) for the full list.

---

## ✨ Features

### Inbox & Notifications
- Dedicated **Inbox** tab mirroring Linear's notifications, with relative timestamps and per-type icons
- Unread badge on the IDE status bar (`Lnr [N]`, capped at `[99+]`); clicking focuses the Inbox
- "Mark all as read", "Archive all", and per-row context menu actions
- Background polling every 60 seconds with optimistic UI updates

### Comments, Reactions & Thread Resolution
- Emoji reactions on comments with a full Unicode picker (search + recently used)
- Reaction pills grouped per emoji, with a tooltip listing reactor names
- Mark a specific reply as the thread's **Resolution**, with a green badge and a `⋮` menu to reopen

### Attachments
- View attachments on issues with MIME-typed icons, size, and uploader name
- Open in browser with a click; right-click to delete
- Upload files via toolbar button or drag-and-drop (25 MB per file)

### Issue Management
- Browse, search, and filter Linear issues directly from the IDE
- Create issues with full field support — title, description, team, state, priority, assignee, project, cycle, and labels
- Edit issues inline — modify all fields without opening Linear
- View and post comments with `Cmd+Enter` / `Ctrl+Enter`
- "All Teams" mode — manage issues across all your Linear teams in one place

### Kanban Board
- **Board view** — columns grouped by workflow state with color-coded headers
- **List view** — collapsible grouped rows in Linear's style
- **Drag-and-drop** to change issue status
- Toggle between views — your preference is remembered across sessions

### AI-Powered Description Generation
- Generate structured issue descriptions from a title and optional context
- **Dual AI provider support:**
  - **JetBrains AI Assistant** — zero configuration, uses your existing AI setup
  - **OpenAI-compatible (BYOK)** — bring your own API key (GPT-4o, Claude, Ollama, etc.)
- Available in both Create Issue and Edit Issue flows

### Git Integration
- Create and auto-checkout branches named after the selected issue
- Copy formatted branch name to clipboard
- Smart commit message prefixing with the current issue identifier

### Cycles & Workflow
- Cycle tracking with progress indicators
- Team selector in the Cycles tab
- Auto-refresh with configurable interval and exponential backoff
- Status bar widget showing Linear connection status

### Issue Templates
- Save frequently used issue configurations as reusable local templates
- Quick-apply from a dropdown in the Create Issue dialog

---

## 🖥 Supported IDEs

Lnr works with **all JetBrains IDEs**:

IntelliJ IDEA · WebStorm · PyCharm · Rider · GoLand · PhpStorm · CLion · RubyMine · DataGrip · DataSpell · Aqua · RustRover · Fleet

---

## 📸 Screenshots

| Issue List | Kanban Board | Create Issue |
|:---:|:---:|:---:|
| ![Issue List](assets/screenshots/screenshot-issue-list.png) | ![Kanban Board](assets/screenshots/screenshot-kanban-board.png) | ![Create Issue](assets/screenshots/screenshot-create-issue.png) |

| Issue Detail | Settings | AI Generate |
|:---:|:---:|:---:|
| ![Issue Detail](assets/screenshots/screenshot-issue-detail.png) | ![Settings](assets/screenshots/screenshot-settings.png) | ![AI Generate](assets/screenshots/screenshot-ai-generate.png) |

| Kanban List | Cycles |
|:---:|:---:|
| ![Kanban List](assets/screenshots/screenshot-kanban-list.png) | ![Cycles](assets/screenshots/screenshot-cycles.png) |

---

## 🚀 Getting Started

### 1. Installation

#### From JetBrains Marketplace (Recommended)

1. Open your JetBrains IDE
2. Go to **Settings** → **Plugins** → **Marketplace**
3. Search for **"Lnr"**
4. Click **Install** and restart your IDE

Or install directly from the [JetBrains Marketplace page](https://plugins.jetbrains.com/plugin/30909-lnr).

#### Manual Installation

1. Download the latest `.zip` from the [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/30909-lnr)
2. Go to **Settings** → **Plugins** → ⚙️ → **Install Plugin from Disk...**
3. Select the downloaded `.zip` file and restart your IDE

---

### 2. Configuration

1. **Get your Linear API Key**: Go to [Linear Settings → API](https://linear.app/settings/api) and create a personal API key.
2. **Configure the IDE**: Open **Settings** → **Tools** → **Lnr**.
3. **Connect**: Paste your API key and click **Test Connection** to verify.
4. **Open Lnr**: Find the **Lnr** icon on the tool window bar (usually on the right) or go to **View → Tool Windows → Lnr**.

---

### 3. AI Setup (Optional)

To enable AI-powered description generation, choose your preferred provider in the Lnr settings:

- **JetBrains AI Assistant** — Zero configuration, uses your existing AI setup (requires AI Assistant plugin).
- **OpenAI-compatible (BYOK)** — Enter your own API key, endpoint, and select a model (GPT-4o, Claude, local models via Ollama, etc.).

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `C` | Create Issue |
| `Ctrl+Shift+B` / `Cmd+Shift+B` | Create Branch |
| `Ctrl+Shift+C` / `Cmd+Shift+C` | Copy Branch Name |
| `O` | Open in Browser |
| `R` | Refresh |
| `Esc` | Close detail panel |

---

## 📋 Requirements

- JetBrains IDE version **2024.1** or later
- [Linear](https://linear.app) account with API key
- Git (for branch creation features)
- JetBrains AI Assistant plugin (optional, for AI generation)

---

## 🐛 Found a Bug?

Please [open an issue](https://github.com/ArtemTykhonuk/LnrPlugin-Public/issues/new?template=bug_report.md) with steps to reproduce. Include your IDE version and Lnr version.

## 💡 Feature Request?

We'd love to hear your ideas! [Submit a feature request](https://github.com/ArtemTykhonuk/LnrPlugin-Public/issues/new?template=feature_request.md).

---

## 📖 Changelog

See [CHANGELOG.md](CHANGELOG.md) for a full list of changes in each version.

---

## 🔒 Technical Details & Privacy

- **Security** — Your Linear API key and AI API keys are stored securely using the IntelliJ Platform's [PasswordSafe](https://plugins.jetbrains.com/docs/intellij/persisting-sensitive-data.html).
- **Privacy** — All API calls are direct to Linear and your AI provider. No middle-man servers are used. Data handling for AI features follows your chosen provider's (JetBrains or OpenAI) policy.
- **Performance** — Built with Kotlin Coroutines and a low-overhead `java.net.http.HttpClient` implementation to ensure a smooth, non-blocking IDE experience.
- **Modern Tech Stack** — Built on the latest Kotlin 2.1 with `kotlinx.serialization` for high-performance GraphQL parsing.
- **Compliance** — See our [Privacy Policy](PRIVACY.md) for full details on how we handle your data and our [Security Policy](SECURITY.md) for reporting vulnerabilities.

---

## 📄 License

Lnr is a proprietary, closed-source plugin. See [LICENSE](LICENSE) for details.

© 2026 Artem Bear. All rights reserved.
