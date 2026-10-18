# 🛡️ AEGIS VAULT — Obsidian Core

> **Military-grade, zero-knowledge, offline-first secure vault.**
> Rebranded from SICE VAULT. 100% client-side. No servers. No tracking.

![Version](https://img.shields.io/badge/version-2.0.0-cyan)
![License](https://img.shields.io/badge/license-MIT-green)
![Security](https://img.shields.io/badge/security-AES--GCM%20%2B%20PBKDF2-blue)
![PWA](https://img.shields.io/badge/PWA-ready-orange)

### ✨ Features
- 🔐 **Master password** with SHA-256 + salt hashing, 5-attempt lockout
- 🔒 **AES-GCM 256 + PBKDF2 100k iterations** for exports
- 📦 **3 item types**: Passwords, Secure Notes, Encrypted Files (up to 10MB)
- 📁 **Custom folders** with emoji
- 🔍 **Instant search** + category filter
- ⏱️ **Auto-lock** after 5 min idle (visual bar)
- 📤 **Encrypted backup / restore** (.vault files)
- 📴 **Offline & PWA** — works without internet, installable
- 🎨 **Obsidian Core UI** — cyber-tactical dark theme

### 🚀 Quick Start (Local)
Just open `index.html` in any modern browser. No build step.

```bash
# Clone
git clone https://github.com/YOUR_USERNAME/aegis-vault.git
cd aegis-vault
# Open
open index.html  # or double-click
```

### 🌐 Deploy to GitHub Pages
1. Push this repo to GitHub
2. Go to Settings → Pages → Source: GitHub Actions
3. The included workflow auto-deploys `index.html`

### 🔧 Tech Stack
- Vanilla HTML/CSS/JS (no dependencies)
- Web Crypto API
- localStorage for persistence (keys: `aegis_vault_data`, `aegis_master_hash`)
- Service Worker for offline

### 📂 Project Structure
```
aegis-vault/
├── index.html              # Main app (single-file, fully functional)
├── manifest.json            # PWA manifest
├── sw.js                   # Service worker
├── README.md
├── LICENSE
├── SECURITY.md
├── CONTRIBUTING.md
├── CHANGELOG.md
├── .gitignore
├── package.json
├── docs/
│   └── ARCHITECTURE.md
└── .github/workflows/pages.yml
```

### 🔒 Security Model
- Master hash never leaves device
- Vault data stored only in localStorage
- Exports are AES-GCM encrypted with user-provided password
- No analytics, no external requests
- Auto-lock on inactivity

### 📜 License
MIT — see LICENSE file.

### 🙏 Credits
Original concept: SICE VAULT
Rebranded & hardened: AEGIS VAULT Obsidian Core (2026)
