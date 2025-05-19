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
- Ubuntu 20.04 (focal) or compatible
- Root or sudo access on the target machine

---

## 📂 Role Variables

These can be overridden in `group_vars`, `host_vars`, or directly in your playbook.

| Variable            | Default     | Description                        |
|---------------------|-------------|------------------------------------|
| `apache_packages`   | `['apache2']`     | List of Apache-related packages to install |
| `php_packages`      | `['php', 'php-mysql']` | PHP packages to install |

---

## 🚀 Example Usage

```yaml
- name: Setup webservers
  hosts: webservers
  become: yes

  roles:
    - vox-x.webservers

