# IIS Setup with Ansible

This repository demonstrates **Windows automation and DevOps skills** by automating IIS installation, default site setup, health-check endpoint, firewall rules, and optional SSL binding using Ansible.

It’s **idempotent**, safe to run multiple times, and ready for deploying static or packaged applications. 
## Features

- Installs IIS with required features:
  - Static Content, Compression, Management Tools, Logging, Health, HTTP Redirects
- Creates default site at `C:\inetpub\wwwroot`
- Adds health check endpoint `/healthcheck.html` (returns `OK`)
- Optional SSL certificate binding on port 443
- Opens Windows Firewall for HTTP/HTTPS
- Ready for static or packaged web applications
- Idempotent: safe to run multiple times

---

## Prerequisites

- Ansible installed on control machine (Linux, Mac, or WSL on Windows)
- WinRM enabled on target Windows server(s)
- Python + pywinrm installed on control machine

---

## Folder Structure


is-ansible/
├─ README.md
├─ .gitignore
├─ playbooks/
│ └─ setup-iis.yml
├─ inventory.ini
└─ files/
├─ placeholder.pfx # Example placeholder for SSL cert
└─ sample-index.html # Optional: sample site file


