<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=250px src=".github/docs/ansible.png" alt="Ansible Linux Hardening Project"></a>
</p>

<h3 align="center">Ansible Linux Hardening | Ubuntu</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)](https://sykesdev.ca/projects/)
[![Lint Status](https://github.com/systemfiles/ansible-linux-hardening/workflows/Lint-CI/badge.svg?event=push)](https://github.com/systemfiles/ansible-linux-hardening/actions?query=workflow%3ALint-CI)
[![GitHub Issues](https://img.shields.io/github/issues/systemfiles/ansible-linux-hardening.svg)](https://github.com/SystemFiles/ansible-linux-hardening/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/systemfiles/ansible-linux-hardening.svg)](https://github.com/SystemFiles/ansible-linux-hardening/issues)
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

## 👷‍♂️ Getting Started

First clone the repository to your Ansible controller

```bash

git clone https://github.com/SystemFiles/ansible-linux-hardening.git; cd ansible-linux-hardening

```

Then, create a copy of the configuration and inventory files from the examples(defaults) provided

```bash

cp ./example.config.yml ./config.yml
cp ./example.inventory.yml ./inventory.yml

```

> Note: for running after the first time, you will likely need to specify a port in your `inventory.yml` file to connect again.

Install some collections that are required by the project using the following `ansible-galaxy` command.

```bash

ansible-galaxy collection install -r requirements.yml

```

Now run the play against your identified hosts

```bash

ansible-playbook main.yml

```

## 👷‍♂️ Authors <a name = "authors" >

- [Ben Sykes (SystemFiles)](https://sykesdev.ca/)