# Security Policy

## Supported Versions
| Version | Supported |
|---------|-----------|
| 2.0.x   | ✅ Yes    |

## Reporting a Vulnerability
Please do NOT open a public issue. Email: security@aegis-vault.local (or open a private advisory on GitHub).

We will respond within 48h.

## Security Features
- Master password hashed with SHA-256 + static salt (client-side)
- Export encryption: AES-GCM 256, PBKDF2 100k iterations, random 16-byte salt + 12-byte IV
- No network requests for vault data
- localStorage only: `aegis_vault_data`, `aegis_master_hash`
- Auto-lock + attempt limiting (5 tries, 30s cooldown)
- CSP-ready, no eval, no inline external scripts except Google Fonts

## Recommendations
- Use 12+ char master password
- Regular encrypted backups
- Do not share .vault files unencrypted
