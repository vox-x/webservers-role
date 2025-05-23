# webservers role

An Ansible role for setting up an Apache web server with PHP and PHP-MySQL support on Ubuntu systems.

## 🧰 Features

- Installs Apache2
- Installs PHP
- Installs PHP-MySQL
- Uses handlers to restart Apache when needed
- Configurable via variables

---

## 📦 Requirements

- Ansible 2.9+
- Ubuntu 24.04 (noble) or compatible
- Root or sudo access on the target machine

---

## 🚀 Example Usage

```yaml
- name: Setup webservers
  hosts: webservers
  become: yes

  roles:
    - vox-x.webservers

