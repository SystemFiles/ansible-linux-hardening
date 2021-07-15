<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=250px src=".github/docs/ansible.png" alt="Ansible Linux Hardening Project"></a>
</p>

<h3 align="center">Ansible Linux Security | Ubuntu</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)](https://sykesdev.ca/projects/)
[![CI](https://github.com/SystemFiles/ansible-linux-security/actions/workflows/ci.yml/badge.svg)](https://github.com/SystemFiles/ansible-linux-security/actions/workflows/ci.yml)
[![CD](https://github.com/SystemFiles/ansible-linux-security/actions/workflows/cd.yml/badge.svg)](https://github.com/SystemFiles/ansible-linux-security/actions/workflows/cd.yml)
[![GitHub Issues](https://img.shields.io/github/issues/systemfiles/ansible-linux-security.svg)](https://github.com/SystemFiles/ansible-linux-security/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/systemfiles/ansible-linux-security.svg)](https://github.com/SystemFiles/ansible-linux-security/issues)
[![License](https://img.shields.io/badge/license-Apache2.0-blue.svg)](/LICENSE)

</div>

---

<p align="center"> An Ansible project to help in securing linux target servers (specifically Ubuntu)
    <br> 
</p>

## 🧐 About <a name = "about"></a>

This Ansible project performs a number of linux hardening tasks on a target or group of targets. This is based off of my own preferences and I am in no way a security expert by any means. **Use at your own risk**

### ⟆ Limitations

- Officially only supports Ubuntu, but may work on other distrobutions as well. It has simply not been tested elsewhere yet.
- Requires some additional collections to function properly (`ansible.posix` and `community.general`)

## 👷‍♂️ Getting Started

First clone the repository to your Ansible controller

```bash

git https://github.com/SystemFiles/ansible-linux-security.git; cd ansible-linux-security

```

Then, create a copy of the configuration and inventory files from the examples(defaults) provided

```bash

cp ./example.config.yml ./config.yml
cp ./example.inventory.yml ./inventory.yml

```

> Note: for running after the first time, you will likely need to specify a port in your `inventory.yml` file to connect again.

Install prerequisite collections via `requirements.yml`

```bash
ansible-galaxy install -r requirements.yml
```

Install the role (can use local via `roles: - '.'`)

```bash

ansible-galaxy install systemfiles.ansible_linux_security

```

Now execute the play against your identified hosts

```bash

ansible-playbook main.yml

```

## 👷‍♂️ Authors <a name = "authors" >

- [Ben Sykes (SystemFiles)](https://sykesdev.ca/)
