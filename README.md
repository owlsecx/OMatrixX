# 🦉 OMatrixX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OWeb-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OMatrixX** — Matrix Synapse Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Matrix Synapse homeserver configuration hardening auditor

---

## ✨ Features

- Offline, read-only audit of Synapse homeserver.yaml (stdlib YAML subset parser with line tracking)
- Registration, shared-secret, macaroon / form secret strength and placeholder detection
- Listener exposure — tls:false on wildcard binds, x_forwarded spoofing, metrics / manhole / replication
- Federation, public-room directory, key-server trust, profile / user-directory privacy checks
- URL-preview SSRF and ip_range_blacklist coverage
- Rate limits, upload size, password policy, bcrypt
- Postgres / SQLite connection checks, signing.key and TLS key permissions, media store permissions
- Workers (workers/*.yaml), log_config, appservices
- nginx / Caddy reverse proxies fronting /_matrix and /_synapse/admin, .well-known / Element JSON files
- coturn turnserver.conf (only when Synapse uses TURN)
- Synapse version EOL hint, CWE + MITRE ATT&CK mapping
- Score + grade A+…F, TXT / MD / JSON / CSV / SARIF
- Hardened templates, --demo self-test, --fail-on

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMatrixX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
