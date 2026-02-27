# CLIProxyAPI Quota - SwiftBar Plugin

A [SwiftBar](https://swiftbar.app/) plugin that displays **Codex** and **Antigravity**
quota usage from your [CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) instance in the macOS menu bar.

## Setup

### 1. Install SwiftBar

```bash
brew install swiftbar
```

### 2. Install the Plugin

Symlink or copy the script to your SwiftBar plugins directory:

```bash
git clone https://github.com/LoveEatCandy/CLIProxyAPI-quota-bar.git
cp CLIProxyAPI-quota-bar/quota.5m.py path/to/SwiftBar/quota.5m.py
```

The `5m` in the filename means SwiftBar refreshes every **5 minutes**.

### 3. Configure Environment Variables

Write `.env` file in the same directory(`path/to/SwiftBar/.env`):

```
CPA_BASE_URL="https://xxx"                # Your CLIProxyAPI server
CPA_MANAGEMENT_KEY="your-management-key"  # Management API key
```

## What It Shows

**Status Bar:**

```
🤖C:100% 🌀A:100%
```

- `🤖C:100%` — 100% Codex quota available
- `🌀A:100%` — 100% Antigravity quota available

**Dropdown Menu:**

- Per-provider account list with quota details
- Status indicators: 🟢 ready / 🔴 rate-limited / 🟡 warning / ⚫ disabled
- Quick links to refresh and open Management Center

## Customization

- Change refresh interval by renaming the file (e.g., `quota.1m.py` for 1 minute)
- Modify `TARGET_PROVIDERS` in the script to track other providers
