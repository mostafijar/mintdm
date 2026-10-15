# OrbitSCP

![Version](https://img.shields.io/badge/version-1.0.9-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)
![Tauri](https://img.shields.io/badge/Tauri-2.11-orange)

<p align="center">
  <img src="build/icons/128x128.png" width="128" alt="OrbitSCP icon">
</p>

Dual-pane workflow focused on speed.
Smooth handling of large directories and large file diffs.
Strong SSH and transfer tooling without heavy setup.

## Features

### Protocols
- SFTP, SCP, FTP, FTPS
- WebDAV / WebDAVS
- Amazon S3 (B2-compatible setups supported)

### File Operations
- Dual-pane file manager
- Split Commander mode (Server A <-> Server B copy)
- Drag and drop upload/download
- Transfer queue manager
- Remote file search
- Permissions editor (chmod/chown)
- Remote path bookmarks
- Last path memory for local pane and both remote panes

### Archive Handling
- Create ZIP archives directly on the server with live file count and percentage
- Extract ZIP archives on the server with live progress
- Progress window with per-file output log

### Safe Batch Delete
- Delete confirmation shows total file count and size before you confirm
- Type DELETE to confirm destructive deletes
- Live per-file delete progress with counts
- Cancel button stops long deletes mid-way, progress window auto-closes when done

### Sync and Compare
- Two-way sync (upload, download, mirror)
- Include-directory filtering for sync scope
- Sync compares real content differences
- 4 compare modes: Smart (Recommended), Fast (size+time), Strict Content (SHA256), Timestamp
- Whitespace-aware compare (toggle) for text files
- Per-file Diff directly from sync result list
- Large-file quick diff preview with highlighted changes
- Diff window opens above sync modal for clear workflow

### Productivity
- Built-in terminal (multi-tab, SSH exec, interactive installer help, resizable, command history)
- Built-in editor
- External editor integration
- Auto-upload on save watcher
- SSH key generation in-app
- Multi-connection tabs
- Session manager (save/import/export)
- Report Issue (top bar & Settings) — guest, no login, rate-limited

### Security and Reliability
- Password and SSH key authentication
- PPK to OpenSSH conversion support
- Host key verification (TOFU)
- SOCKS5 proxy support
- Keepalive and auto-reconnect behavior
- Optional transfer integrity verification
- Connection and transfer timeouts — no more endless hangs on dead servers
- Atomic downloads and safer resume handling across protocols
- Per-connection bandwidth throttle
- Resumable uploads for all protocols (SFTP/SCP/FTP/FTPS/S3/WebDAV) with `..orb~up` part files

## Installation

### Windows
Download the latest .exe installer from the Releases page.

### Linux

| Format | Distros |
|--------|---------|
| .deb | Ubuntu, Linux Mint, Debian |
| .rpm | Fedora, CentOS, RHEL, openSUSE |
| .AppImage | Universal, no install needed |

Download from the Releases page and install with your package manager.

### macOS
Download the latest .dmg from the Releases page.

## Uninstall

```bash
# DEB (Ubuntu / Debian / Mint)
sudo apt remove orbitscp

# RPM (Fedora / RHEL / CentOS)
sudo dnf remove orbitscp

# RPM (openSUSE)
sudo zypper remove orbitscp

# Optional: remove app data
rm -rf ~/.config/orbitscp
rm -rf ~/.local/share/orbitscp
rm -rf ~/.orbitscp
```

## OrbitSCP vs the rest

| Area | OrbitSCP | WinSCP | FileZilla |
|---|---|---|---|
| Protocols (SFTP/SCP/FTP/FTPS/WebDAV/S3) | ✅ all free | ✅ | ❌ S3 is paid |
| Transfer safety (atomic writes, integrity check) | ✅ | ➖ | ➖ |
| Queue with priorities | ✅ | ✅ | ✅ |
| Batch delete with live progress + cancel | ✅ | ❌ | ❌ |
| Server-side ZIP create + extract | ✅ | ❌ | ❌ |
| Server A ↔ Server B direct copy | ✅ | ❌ | ❌ |
| Sync with SHA256 content compare | ✅ | ➖ | ❌ |
| Built-in diff viewer | ✅ | ❌ | ❌ |
| Built-in SSH terminal (multi-tab) | ✅ | ❌ | ❌ |
| Built-in editor + auto-upload on save | ✅ | ❌ | ❌ |
| In-app SSH key generation | ✅ | ❌ (needs PuTTYgen) | ❌ |
| Scripting / scheduled sync | ❌ | ✅ | ❌ |
| Master password | ❌ | ✅ | ❌ |
| Windows / macOS / Linux | ✅ | ❌ Windows only | ✅ |

## Contributing
Pull requests are welcome. For bugs and feature ideas, use **Report** in the app or open an issue at Issues.

## Author
Mostafijar Rahman
GitHub · Email

If OrbitSCP helps you, a star on GitHub is appreciated.
