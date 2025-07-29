
# ⚔️ Python SSH Botnet – Remote Command Execution Tool

A Python-based SSH botnet controller for remote command execution across multiple Linux systems. Designed for red team labs, adversary simulation, and ethical hacking practice.

> ⚠️ For educational use only.

---

## 📌 Features

- 🔐 SSH login automation using `pxssh`
- 📡 Remote command execution on all bots
- 🐚 Interactive bash on remote hosts
- 💾 Persistent botnet state (`botnet.json`)
- 💥 Basic DDoS simulation using Scapy
- 🎨 Color-coded CLI menu using Colorama

---

## 🚀 Getting Started

### 🔧 Requirements

```bash
pip install pexpect colorama scapy
```

Ensure the target bots:
- Run OpenSSH
- Allow password-based login
- Are accessible on the network

---

## 📁 File Structure

```
ssh_botnet.py        # Main controller script
botnet.json          # (Auto-saved) Bot credentials & session info
```

---

## 🎯 Usage

```bash
python ssh_botnet.py
```

### 🖥️ Main Menu

```
1. List Bots
2. Run Command
3. Bash
4. Add Bot
5. DDOS
6. Exit
```

---

## 📦 Add a Bot

```bash
Enter the bot's IP address: 192.168.1.101
Enter the bot's SSH port number: 22
Enter the bot's username: user
Enter the bot's password: pass123
```

Bot will be stored in `botnet.json`.

---

## 💥 DDoS (Test Lab Only)

Floods a test target with SYN packets using `Scapy`:

```python
IP(dst="192.168.10.140") / TCP(dport=80, flags="S") / Raw("X"*1024)
```

Use responsibly in **isolated lab environments** only.

---

## 🔐 Legal Disclaimer

This tool is developed for:

- ✅ Ethical hacking labs
- ✅ Red/Blue team simulations
- ✅ Cybersecurity education

Do **NOT** use on unauthorized networks or systems. Misuse may violate laws.

---

## 🙋 Created By

**Rajkumar Kumawat**

- 🔗 [LinkedIn](https://www.linkedin.com/in/rajkumar-kumawat-66072b199/)
- 🐙 [GitHub](https://github.com/Rjkumarkumawat)
- ✍️ [Medium](https://medium.com/@rajkumarkumawat.workup)

Follow for more red team and cybersecurity tools built with Python ⚙️

---

## 🏷️ Tags

`Red Team` • `SSH Automation` • `Remote Command Execution` • `Python Botnet` • `Ethical Hacking`
