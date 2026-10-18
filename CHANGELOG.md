# Changelog

## 2.0.0 - 2026-10-18 - AEGIS Rebrand
- Renamed from SICE VAULT to **AEGIS VAULT — Obsidian Core**
- Fixed XSS in folder rendering (now escaped)
- Fixed fileData persistence on edit
- Replaced insecure Math.random() with crypto.getRandomValues() for password gen
- Improved escAttr escaping
- Added fileSize tracking
- Migrated storage keys to `aegis_*` namespace
- Added PWA manifest + service worker
- Added GitHub Pages workflow
- Improved responsive design
- Min 8 char master password enforced
- New README, LICENSE, SECURITY docs

## 1.0.0 - Original SICE VAULT
- Initial vault with passwords, notes, files
- AES-GCM export/import
- Auto-lock
