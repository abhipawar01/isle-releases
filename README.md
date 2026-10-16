# Isle

**A tiny cat that keeps an eye on Claude.**

Isle is a small floating pill for your desktop. It shows what [Claude Code](https://www.anthropic.com/claude-code) is
doing right now, and lets you answer its permission requests (**Allow** or **Deny**) with one click, without hunting
for the terminal.

> **Private beta.** Isle is being tested by a small group. It works on **Windows 10+** and **macOS 12+**.
> This repository only hosts the installers; the source code is not published here.

## Download

Go to the [**latest release**](https://github.com/abhipawar01/isle-releases/releases/latest) and pick the file for your computer:

| Your computer | File |
| --- | --- |
| Windows | `Isle-<version>-win-setup.exe` |
| Mac with Apple silicon (M1, M2, M3, M4) | `Isle-<version>-mac-arm64.dmg` |
| Mac with an Intel chip | `Isle-<version>-mac-x64.dmg` |

Not sure which Mac you have? Apple menu → **About This Mac**: "Chip: Apple M…" means Apple silicon, "Processor: Intel…" means Intel.

If there is no release yet, the beta has not opened. Check back soon.

## Install

These builds are **not code-signed yet**, so your computer will warn you the first time. That is expected.

### Windows

1. Run the `.exe`.
2. If Windows says **"Windows protected your PC"**, click **More info → Run anyway**.
3. Isle installs for your user only (no administrator needed) and starts.

### macOS

1. Open the `.dmg` and drag **Isle** into **Applications**.
2. Open Isle with **right-click → Open → Open** (a normal double-click is blocked for unsigned apps).
3. If macOS still refuses, run this once in Terminal, then open Isle again:

   ```
   xattr -cr /Applications/Isle.app
   ```

Isle lives in the **menu bar** (there is no Dock icon): look for the cat at the top of the screen.

## First use

1. Click the pill to open the dashboard and press **Connect** next to "Connect Claude Code". This adds Isle's hooks to
   Claude Code. No Node.js is needed.
2. Use Claude Code as usual, in your terminal or in your editor. Isle shows what it is doing.
3. When Claude asks for permission, the pill shows **✕ / ✓**. Click one, or answer in the terminal as you normally would.
   Whichever you answer first wins.

Isle never approves anything by itself: if you do not answer within 60 seconds, Claude simply asks you in the terminal.

## Privacy

- Nothing about you or your work is uploaded. Isle talks to Claude Code on your own computer.
- Its only outside request is an optional check for a newer version (a plain request to this repository's releases).
  You can switch it off in the **⋯** menu.
- Logs stay in `~/.isle/logs`. A diagnostics report is only copied to your clipboard when you ask for it.

## Uninstall

- **Windows:** uninstall Isle from Settings → Apps. It removes its hooks from Claude Code too.
- **macOS:** open the **⋯** menu and choose **Disconnect Claude Code** first, then drag Isle to the Bin.

## Feedback and problems

Please [open an issue](https://github.com/abhipawar01/isle-releases/issues). If something went wrong, open the **⋯** menu, choose **Copy diagnostics**, and
paste the report into the issue. It contains no secrets, and you can read it before sharing.

---

Isle is an independent project and is not affiliated with or endorsed by Anthropic. Claude and Claude Code are
trademarks of Anthropic. © 2026 Isle.
