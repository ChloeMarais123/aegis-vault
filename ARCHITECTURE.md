# AEGIS VAULT Architecture

## Overview
Single-page application, 100% client-side. No backend.

## Data Flow
```
[Lock Screen] --hash--> localStorage:aegis_master_hash
[App] --CRUD--> localStorage:aegis_vault_data (JSON)
[Export] vault JSON --PBKDF2+AES-GCM--> .vault file
[Import] .vault file --decrypt--> vault JSON
```

## Crypto
- Master: SHA-256(password + salt) stored
- Export: PBKDF2 100k + AES-GCM 256 + random salt/iv

## Components
- Lock screen: first-time detection via missing hash
- Sidebar: view filter + folder filter
- Grid: search + render
- Modals: add/edit/view
- Auto-lock: mousemove/keydown resets timer

## Storage Schema
```json
{
  "items": [{ "id","type","name","username","password","url","notes","content","fileData","fileSize","folder","created" }],
  "folders": [{ "id","name","emoji" }]
}
```

## Future
- WebAuthn unlock
- Argon2 option
- E2E sync via WebRTC
