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

OMatrixX is an offline, read-only Matrix Synapse homeserver configuration auditor. It parses `homeserver.yaml` (stdlib YAML subset), related workers, reverse proxies, well-known files, and coturn when TURN is configured. It reviews registration, secrets, listeners, federation, SSRF, media, rate limits, and TLS key permissions with score/grade and multi-format export.

---

## ✨ Features

- Offline audit of Synapse homeserver.yaml with line-tracked stdlib YAML subset parser
- Registration, shared-secret, and macaroon/form secret strength and placeholder detection
- Listener exposure (tls:false on wildcards, x_forwarded, metrics/manhole/replication)
- Federation, public-room directory, key-server trust, profile/user-directory privacy, URL-preview SSRF
- Workers, log_config, appservices, nginx/Caddy fronting `/_matrix`, well-known/Element JSON, coturn TURN
- Score/grade, templates, CWE+ATT&CK mapping, TXT/MD/JSON/CSV/SARIF, `--demo` and fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OMatrixX -c homeserver.yaml --scan
./OMatrixX --root ./synapse -f sarif -o matrix.sarif --fail-on high
./OMatrixX --demo --list-rules
./OMatrixX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
