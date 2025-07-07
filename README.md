# 📦 Ansible Playbooks – Basic Application Installation

Welcome to this repository containing **Ansible playbooks** for automating the basic installation of common applications on servers.

The purpose of this project is to:
- Save time when provisioning new environments
- Standardize application setup
- Use a clean, isolated Python environment with Ansible

> ⚠️ **Note:** These playbooks are intended for use on real **Red Hat-based operating systems** such as:
> - Red Hat Enterprise Linux (RHEL)
> - CentOS
> - Rocky Linux
> - AlmaLinux

They may not work properly on non-RHEL-based systems like Debian, Ubuntu, or containers that lack `systemd`.

---

## 🚀 Getting Started

### 1. Create a Python virtual environment

```bash
python3 -m venv ansible
source ./ansible/bin/activate
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

---

### 🔧 Maintain environment

When your virtual environment is active:
```bash
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

---

### 📁 Project Structure

```
.
├── ansible/                 # Virtual environment (not versioned)
├── playbooks/
│   ├── install_nginx.yml
│   ├── install_docker.yml
│   └── ...
├── inventory/
│   └── hosts.ini
├── roles/
│   ├── example_role.yml
├── templates/
│   └── example.conf.j2
├── requirements.txt
└── README.md
```

---

### ▶️ Running a Playbook

```
ansible-playbook -i inventory/hosts.ini playbooks/install_nginx.yml
```




