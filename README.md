# Kodio Studio - AI-Powered Collaborative Coding in VS Code


**Transform your coding workflow with AI-powered code generation and real-time collaboration, directly in Visual Studio Code.**

Kodio Studio brings intelligent code generation, workspace sharing, and live collaboration features to your favorite IDE. Generate code with AI, share your entire workspace with teammates, and code together in real-time with cursor sharing and file locking.

![Kodio Studio Extension](https://raw.githubusercontent.com/InfiltratorFitting/kodio-smart-forge/main/images/kodio-vscode-collaboration-demo.png)

## 🎬 See It In Action

**[📺 Watch 2-Minute Demo Video](https://kodio.ai/demo)** | **[🚀 Try It Free at kodio.ai](https://kodio.ai)**

*Quick preview: Generate AI code in seconds, share your workspace with one command, see teammates' cursors in real-time.*

## ✨ Key Features

### 🤖 AI-Powered Code Generation
- **Built-in Language Model** - Kodio registers its own Language Model Provider, so AI features work in any VS Code-compatible editor (including code-server) — no GitHub Copilot required
- **Kodio AI Chat Panel** - A dedicated chat panel with its own activity bar icon (💬), separate from the file explorer, with all 17 commands
- **Works Everywhere** - Full functionality in code-server, VS Code OSS, and VS Code Desktop
- **Real File Creation** - `/agent`, `/template`, and `/multi` actually create files on disk (not just text output)
- **Multi-Language Support** - Python, JavaScript, TypeScript, Java, C++, Go, Rust, and more
- **Context-Aware** - AI understands your project structure and coding style

### 💬 @kodio Chat Assistant & AI Chat Panel

All commands work in both the `@kodio` chat participant and the **Kodio AI Chat** panel (💬 icon in activity bar).

**Code Generation**
- **`/generate`** - Generate new code from natural language
- **`/multi`** - Scaffold multiple related files at once
- **`/template`** - Quick-start from pre-built project templates

**Code Improvement** (reads active editor selection)
- **`/modify`** - Modify selected code with instructions
- **`/fix`** - Diagnose and fix bugs in selected code
- **`/optimize`** - Improve code performance

**Understanding** (reads active editor selection)
- **`/explain`** - Get clear explanations of selected code
- **`/test`** - Auto-generate unit tests for selected code

**Agentic Workflows** (with live Workflow Progress panel)
- **`/agent`** - Execute complex multi-step workflows with AI planning — creates real files on disk
- **`/plan`** - View active workflow plans
- **`/continue`** - Continue a paused workflow
- **`/rollback`** - Rollback to a checkpoint

**Team Collaboration**
- **`/createteam`** - Create a new team project
- **`/jointeam`** - Join a team project with an invitation code
- **`/viewteam`** - View your team projects and members
- **`/teamcontext`** - Browse shared team AI context

- **`/help`** - See all available commands

### 🤝 Real-Time Collaboration (Live Share Alternative)
- **Workspace Sharing** - Share your entire VS Code workspace with one command
- **Live Cursor Tracking** - See exactly where teammates are typing in real-time
- **File Locking** - Prevent conflicts with automatic file lock management
- **Presence Awareness** - Know who's online and what files they're viewing
- **External Project Support** - Collaborate on projects outside your workspace

### 🌳 Smart Workspace Browser
- **Hierarchical Navigation** - Browse workspaces → sessions → documents in tree view
- **Real-time Sync** - Automatically refreshes when new code is generated
- **Quick Access** - One-click to open any document in editor
- **Search & Filter** - Find documents instantly across all workspaces

### 📄 Professional Document Management
- **Automatic Syntax Highlighting** - Detects language and applies proper formatting
- **Save to Local** - Right-click any document to save to your file system
- **Version History** - Track changes across AI generation sessions
- **Batch Operations** - Save multiple documents at once

### 🔐 Enterprise-Grade Security
- **Encrypted Storage** - JWT tokens stored in VS Code's secure SecretStorage
- **Status Bar Integration** - See login status at a glance (✓/✗ Kodio)
- **One-Click Authentication** - Sign in securely from within VS Code
- **Automatic Token Refresh** - Stay logged in without interruption

## 🎯 Perfect For

- **Solo Developers** - Generate boilerplate code instantly, focus on complex logic
- **Remote Teams** - Pair program with colleagues anywhere in the world
- **Code Reviews** - Review AI-generated code with full IDE features
- **Learning** - Study AI-generated examples with IntelliSense and debugging
- **Rapid Prototyping** - Build MVPs 10x faster with AI assistance
- **Open Source** - Collaborate with contributors in real-time

## 📦 Installation

### Method 1: VS Code Marketplace (Recommended)
1. Open VS Code
2. Press `Ctrl+Shift+X` to open Extensions panel
3. Search for **"Kodio Studio"**
4. Click **Install**
5. Reload VS Code

### Method 2: One-Click Install
[Install from VS Code Marketplace →](https://marketplace.visualstudio.com/items?itemName=traluven.kodio-smart-forge)

### Method 3: From .vsix File
1. Download `kodio-vscode-extension-0.9.14.vsix`
2. Open VS Code → Press `Ctrl+Shift+P`
3. Type "Install from VSIX" → Select the file

## 🚀 Quick Start Guide

### Step 1: Create Your Free Account
1. Visit [kodio.ai](https://kodio.ai) and sign up (takes 30 seconds)
2. No credit card required for free tier

### Step 2: Login in VS Code
1. Click the **Kodio Studio** icon in Activity Bar (left sidebar) for workspace management
2. Click the **💬 Chat** icon in Activity Bar for AI Chat and Workflow Progress
3. Click **"Login to Kodio"** in the TreeView
4. Enter your credentials → Status bar shows **✓ Kodio**

### Step 3: Generate Your First AI Code
1. Go to [kodio.ai/studio](https://kodio.ai/studio)
2. Describe what you want: *"Create a React todo list component with TypeScript"*
3. AI generates the code → Returns to VS Code extension
4. Click the document to open in editor → Save to your project

### Step 4: Share & Collaborate (Optional)
1. Open any project folder in VS Code
2. Press `Ctrl+Shift+P` → Type "Kodio: Share Current Workspace"
3. Share the session ID with teammates
4. They join → See each other's cursors in real-time

### Pro Tips
- Use `Ctrl+Shift+P` → "Kodio" to see all commands
- Right-click documents for quick actions
- Click refresh icon to sync latest AI generations

## ⚙️ Configuration

The extension uses **production URLs by default** and works out-of-the-box. No configuration needed for most users.

Configure via VS Code settings (`Ctrl+,` → search "Kodio"):

| Setting | Description | Production Default |
|---------|-------------|---------|
| `kodio.backendBaseUrl` | Kodio backend API URL | `https://kodio-backend.purplefield-13215ae2.westus.azurecontainerapps.io` |
| `kodio.webAppUrl` | Kodio web app URL | `https://kodio.ai` |
| `kodio.enableTelemetry` | Send anonymous usage data | `false` |

### 🔧 Development Mode (Localhost)

If you're running Kodio backend locally for development, configure these settings:

**Option 1: Via Settings UI**
1. Press `Ctrl+,` to open Settings
2. Search for "Kodio"
3. Set `Backend Base URL` to `http://localhost:5000`
4. Set `Web App URL` to `http://localhost:3001`

**Option 2: Via settings.json**
```json
{
  "kodio.backendBaseUrl": "http://localhost:5000",
  "kodio.webAppUrl": "http://localhost:3001"
}
```

**Option 3: Workspace-specific settings**
Create `.vscode/settings.json` in your project root:
```json
{
  "kodio.backendBaseUrl": "http://localhost:5000",
  "kodio.webAppUrl": "http://localhost:3001"
}
```

### 🌐 Production Mode (Default)

Extension connects to production servers by default. No configuration needed:
- **Backend**: https://kodio-backend.purplefield-13215ae2.westus.azurecontainerapps.io
- **Frontend**: https://kodio.ai

## 💡 Real-World Use Cases

### Scenario 1: Rapid API Development
*"I need a RESTful API with authentication"*
- Generate FastAPI/Express boilerplate with AI
- Open in VS Code → Review with IntelliSense
- Add custom business logic → Deploy in minutes

### Scenario 2: Remote Pair Programming
*Two developers, different time zones*
- Developer A shares workspace from VS Code
- Developer B joins → sees cursor movements live
- File locks prevent conflicts → seamless collaboration
- No screen sharing lag or video call needed

### Scenario 3: Code Review & Learning
*Junior dev generates React component*
- AI creates component → Senior dev reviews in VS Code
- Suggests improvements → Junior sees changes live
- Learn best practices through real-time mentorship

### Scenario 4: Open Source Contribution
*Contributing to GitHub project*
- Fork repository → Share workspace with maintainer
- Maintainer guides you through codebase
- See their cursor navigate code → understand context
- Submit better PR with real-time feedback

## 📋 Requirements

- **VS Code Version**: 1.95.0 or higher (for built-in Language Model support)
- **code-server**: v4.x+ supported (uses webview chat panel instead of Copilot Chat)
- **Kodio Account**: Active account on Kodio Studio platform
- **Backend Access**: Kodio backend must be accessible (local or cloud)

## 🐛 Known Issues

- **WebSocket Support**: Real-time document updates not yet implemented (manual refresh required)
- **Editing Limitations**: Documents are read-only; edit in Kodio Studio web app
- **Large Files**: Documents over 10MB may load slowly

## 🔒 Privacy & Security

- **Credentials**: Stored securely using VS Code's `SecretStorage` API (encrypted)
- **JWT Tokens**: Automatically refreshed, never logged or transmitted insecurely
- **Telemetry**: Disabled by default; opt-in via settings if you want to help improve the extension

## 🛠️ Troubleshooting

### "Failed to fetch workspaces"
- **Solution**: Check `kodio.backendBaseUrl` points to correct backend URL
- Verify you're logged in (status bar shows ✓ Kodio)
- Ensure backend is running and accessible

### "Login failed"
- **Solution**: Verify username/password are correct
- Check backend URL is correct
- Try logging out and logging back in

### Documents not showing
- **Solution**: Click the **Refresh** icon in TreeView header
- Verify session contains documents in Kodio web app
- Try logging out and back in to refresh token

### Cannot save to workspace
- **Solution**: Ensure you have write permissions to selected folder
- Check file doesn't already exist (will prompt to overwrite)
- Verify document content is not empty

## 🗺️ Roadmap

### Coming Soon
- ✅ TreeView navigation (Completed)
- ✅ Authentication & secure storage (Completed)
- ✅ Document viewing (Completed)
- ✅ Save to workspace (Completed)
- 🔄 Real-time document updates via WebSocket
- 🔄 In-editor collaboration (locks, presence)
- 🔄 Search & filter documents
- 🔄 Language-specific file icons
- 🔄 Document preview on hover

## 🤝 Contributing

We welcome contributions! Here's how to help:

1. **Report Bugs**: Open an issue on GitHub with reproduction steps
2. **Suggest Features**: Create a feature request issue
3. **Submit PRs**: Fork the repo, make changes, submit pull request

## 📄 License

This extension is licensed under the [MIT License](https://github.com/nsingh2510/kodio/blob/HEAD/LICENSE).

## � Why Developers Love Kodio

> "Generated a complete Python FastAPI backend in under 2 minutes. This is insane!" - *@devjohn*

> "Finally, a Live Share alternative that actually works. Cursor tracking is smooth as butter." - *@sarah_codes*

> "Best AI code generation I've tried. Understands context way better than competitors." - *@techwriter*

## 🔗 Links & Resources

- 🌐 **Website**: [kodio.ai](https://kodio.ai)
- 🚀 **Web App**: [kodio.ai/studio](https://kodio.ai/studio)
- 📖 **Documentation**: [docs.kodio.ai](https://docs.kodio.ai) (coming soon)
- 💬 **Discord Community**: [Join our Discord](https://discord.gg/kodio) (coming soon)
- 🐛 **Report Issues**: [GitHub Issues](https://github.com/nsingh2510/kodio/issues)
- 📧 **Support**: support@kodio.ai
- 🐦 **Twitter**: [@KodioAI](https://twitter.com/kodioai) (coming soon)

## ❤️ Acknowledgments

Built with:
- [Visual Studio Code Extension API](https://code.visualstudio.com/api)
- [TypeScript](https://www.typescriptlang.org/)
- [Socket.IO](https://socket.io/) (coming soon)

---

**Made with ❤️ by the Kodio Team**

*Empowering developers with AI-powered collaborative coding*
