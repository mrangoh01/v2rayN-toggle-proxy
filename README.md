# 🛰️ v2rayN Toggle Proxy for Ubuntu (VirtualBox)

A lightweight Bash script that automatically enables or disables system-wide proxy settings in Ubuntu (running inside VirtualBox) based on the status of *v2rayN* on the Windows host.

When v2rayN is active on Windows, this script detects it and configures Ubuntu to route all traffic (including apt, snap, git, curl, etc.) through the same proxy.  
When it’s off, the script restores normal direct connection automatically.

---

## ✨ Features

- 🔍 Auto-detects whether v2rayN is running  
- 🔁 Enables/disables proxy for:
  - Shell / Terminal
  - apt package manager
  - snap
  - git, curl, wget, pip
- 🧠 Smart HTTPS connectivity check (solves SSL error issues)
- 🪵 Creates logs at /var/log/toggle-proxy.log
- 🧰 Works perfectly with VirtualBox NAT or Bridge network modes

---

## ⚙️ Installation

1. Copy the script into /usr/local/bin:

   ```bash
   sudo nano /usr/local/bin/toggle-proxy
2. Make it executable:

   ```bash
   sudo chmod +x /usr/local/bin/toggle-proxy
4. Run automatically at terminal startup(Optional):
   
   ```bash
   echo "toggle-proxy" >> ~/.bashrc
   
## Notes

1.Check the v2rayN using ports on Host machine (default 10808 for https & 10809 for socks5)
2.Since I wasn't proficient in Bash Scripting yet, I got little helps from GPT:D

## Log files
log saved in:
  "/var/log/toggle-proxy.log"

## Usage
simply run:

   ```bash
   toggle-proxy
