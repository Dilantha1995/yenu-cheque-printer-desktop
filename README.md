# Yenu Cheque Printer — Desktop

A desktop build of the [Yenu Cheque Printer](https://www.yenuit.com/tools/cheque-printer) tool, wrapped with Electron so it installs and runs as a native app, with no browser or internet connection required to print a cheque.

Same features as the web version: ~98 banks across Maldives, Sri Lanka, India and UAE, drag-to-align fields, per-bank saved layouts/fonts/crossing style, a payee register, and a cheque register — all stored locally on this computer.

## Install

Download the latest installer for your OS from [Releases](../../releases):

- **Windows** — `Yenu-Cheque-Printer-Setup-<version>.exe` (installer) or the portable `.exe`
- **Linux** — `.AppImage` (run directly) or `.deb` (install via package manager)
- **macOS** — `.zip` (unzip to get `Yenu Cheque Printer.app`). This build is unsigned/not notarized, so the first launch needs *right-click → Open* to bypass Gatekeeper, or `xattr -cr "Yenu Cheque Printer.app"` in Terminal.

## Development

```bash
npm install
npm start          # run the app
npm run dist:win    # build the Windows installer + portable exe
npm run dist:linux   # build the Linux AppImage + deb
npm run dist         # build for the current platform
```

The app itself is a single page at `app/index.html` — the same file shipped on the website, loaded locally instead of over the network.
