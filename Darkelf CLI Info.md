# 🧠 Darkelf CLI Browser – Post-Quantum OSINT & Secure Tor Terminal

Darkelf CLI is a post-quantum hardened OSINT browser and messaging platform for adversarial or censorship-heavy environments. Designed for operatives, researchers, and red teamers, it provides powerful reconnaissance and secure communication with memory-safe features and zero-API intelligence gathering.

---

## ⚙️ Features Overview

| Category                     | Description                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| 🔐 **Post-Quantum Messaging**  | ML-KEM-768 + Fernet hybrid encryption for encrypted CLI messaging            |
| 🌐 **Tor-Based Browser**       | Full-text HTML browser routed over Tor (SOCKS5h proxy via obfs4 or standard) |
| 🔎 **Darkelf OSINT Engine**   | Phone & email recon: carrier, location, VoIP check, timezones, no APIs       |
| 🧠 **Phishing Detection**     | Heuristic scanning for malicious patterns, typosquatting & spoofed domains   |
| 💀 **Panic Mode**             | Erases logs, memory dumps, clears env state, triggers decoy traffic         |
| 🎭 **Stealth Enhancements**   | Memory locking, header spoofing, random jitter, decoys, sandbox detection    |
| 🧪 **Log Encryption**         | AES-GCM logs encrypted in memory using PQC-derived secrets                   |
| 🧩 **Tool Launcher**          | Launch recon tools like `nmap`, `amass`, `shodan`, `whatweb`, `dmitry`       |
| 🕵️ **.onion Search Engine**   | Onion site discovery via Ahmia and DDG onion mirror queries                  |
| 📱 **Phone OSINT**            | Detect validity, carrier name, VoIP status, leaks (no PhoneInfoga used)     |
| ✉️ **Email Intelligence**     | DNS/MX, RDAP, disposable checks, breaches, gravatar hash, TXT records       |

---

## 🧰 Modules Included

- **Encrypted Messenger:** CLI-based secure communication with hybrid PQ+Symmetric encryption.
- **OSINT Engine:** Performs recon using only public Tor and DuckDuckGo onion-lite searches.
- **Phone Analyzer:** Validity, region, carrier detection, and potential disposable number checks.
- **Email Scanner:** Domain checks, breach results, and DNS intelligence—without using APIs.
- **Memory-Hardened Browser:** Fetch and parse web content securely from `.onion` and clearnet.
- **Tool Hub:** Launches external OSINT tools from a unified REPL interface.
- **Tor Beacon & Onion Validation:** Pings `.onion` services for uptime and status checks.
- **Fake Traffic Generator:** Background activity simulation to confuse behavioral forensics.

---

## 🔧 Installation

### 1. Dependencies

Install Tor & Python 3.11:

```bash
# Debian/Ubuntu
sudo apt install tor python3.11

# macOS (using brew)
brew install tor python@3.11
```

### 2. Python Modules

```bash
pip install -r requirements.txt
```

---

## 🚀 Getting Started

```bash
python3.11 Darkelf_CLI_TL_Edition_Patched_FINAL_FIXED_WORKING.py
```

Use the REPL prompt for commands like:

- `search <query>` — DuckDuckGo .onion search
- `osintscan <phone|username>` — OSINT scan on target
- `message send` — Start encrypted messaging
- `panic` — Trigger panic mode
- `launch <tool>` — Run an integrated OSINT utility
- `beacon <onion>` — Check onion site status
- `exit` — Quit securely

---

## ✅ Supported Platforms

- ✅ macOS (Apple Silicon M1–M4)
- ✅ Linux (Debian, Arch, Fedora)
- ✅ Windows (WSL2 Recommended)
- ✅ Android (via Termux)

---

## 🔐 Security Model

- Encrypted logs are stored only in memory (`AES-GCM`) and purged on exit.
- All metadata stays local; no 3rd-party OSINT APIs like Numverify or PhoneInfoga are used.
- All search is routed through `DuckDuckGo Onion Lite` to bypass tracking & geofiltering.
- Carrier and location data is inferred offline using `phonenumbers`, `geocoder`, and `timezone`.

---

## 📝 Licenses & Attributions

This project includes:

- `psutil` — BSD 3-Clause
- `rich` — MIT
- `beautifulsoup4` — MIT
- `requests` — Apache 2.0
- `cryptography` — Apache 2.0
- `phonenumbers` — Apache 2.0
- `liboqs` & `pyoqs` — BSD & MIT (Post-Quantum Crypto)
- `stem` — Tor control interface

---

## 📫 Feedback & Contributions

Feel free to submit issues, patches, or modules. All tooling is designed with privacy, auditability, and operational flexibility in mind.

---

**Built for those who operate in the shadows.** 🕶  
Stay quiet. Stay hardened. Stay Darkelf.
