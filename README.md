# 🐳 Ansible-Docker Lab

Spin up a tiny lab with one **Ansible Controller** and four **SSH-enabled nodes** (`web01`, `web02`, `db01`, `db02`)—all in Docker.  
Perfect for practising playbooks, testing roles, or demoing Ansible concepts without touching real servers.

---

## ✨ Features
- **Controller + 4 Nodes** on a single Docker bridge network  
- Ready-to-use password login (`ansible/ansible`)  
- `id_rsa` volume-mapped so you can switch to key-based auth instantly  
- Minimal example **playbook.yml** that pings every host

---

## 🗺️ Directory Layout  
*(everything lives in the project root—no sub-folders)*

```text
.
├── Dockerfile.controller   # Image for the Ansible controller
├── Dockerfile.node         # Image reused by all nodes
├── docker-compose.yml      # Spins up the full lab
├── ansible.cfg             # Ansible configuration
├── hosts.ini               # Inventory (web & db groups)
├── playbook.yml            # Basic ping playbook
└── id_rsa                  # Placeholder private key (replace!)
