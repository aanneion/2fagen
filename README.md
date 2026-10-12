# 🔐 Authenticator

> A modern, offline, zero-knowledge 2FA code generator that runs entirely in your browser. No accounts. No servers. No tracking. Your secrets never leave your device.

![License](https://img.shields.io/badge/license-MIT-green)
![No Dependencies](https://img.shields.io/badge/dependencies-1-brightgreen)
![Encryption](https://img.shields.io/badge/encryption-AES--256--GCM-success)

## ✨ Features

- 📷 **QR code scanning** — point your camera at any TOTP QR (Google Authenticator, Authy, etc.)
- ⌨️ **Manual entry** — paste Base32 secrets or `otpauth://` links
- 🔢 **Live TOTP codes** — RFC 6238 compliant, auto-refreshing countdown ring
- 🔒 **AES-256-GCM encrypted vault** — your secrets are never stored in plaintext
- 🛡️ **PIN/password lock** — vault auto-locks after inactivity (1/5/15/30 min or never)
- 🔑 **PBKDF2 key derivation** — 150,000 iterations, SHA-256, random salt
- 📦 **Backup & restore** — plain or password-encrypted JSON export/import
- 🌓 **Dark & light green theme** — auto-detects system preference
- 📱 **Fully responsive** — mobile-first, native-app feel
- ⚡ **100% client-side** — single HTML file, host anywhere

## 🛠 Tech Stack

- Vanilla JavaScript (no framework)
- Web Crypto API (AES-256-GCM + PBKDF2)
- [jsQR](https://github.com/cozmo/jsQR) for QR scanning
- RFC 6238 TOTP (HMAC-SHA1)

## 🚀 Deploy

1. Download `index.html`
2. Host on GitHub Pages / Netlify / Vercel / any static host
3. Open in a browser — done.

**Note:** Camera access requires HTTPS (or `localhost`).

## ⚠️ Security Notes

- All encryption happens **locally** in your browser
- Your PIN is never stored — only a PBKDF2-derived key, held in memory while unlocked
- Forgetting your PIN means your data **cannot be recovered** (by design)
- Always keep an encrypted backup file in a safe place

## 📄 License

MIT

---

Made with ❤ by [Neion](https://fb.com/aanNEION)
