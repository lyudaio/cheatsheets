# Ansible Cheatsheet - Latest LTS (2.13 as of 2021-09 Cutoff)

## Introduction

Ansible is an open-source IT automation platform that helps you manage your infrastructure and applications. Ansible uses a simple syntax written in YAML, known as playbooks, to describe automation jobs, and executes these playbooks using the `ansible-playbook` command.

## Installation

To install Ansible, you can follow the instructions provided in the official documentation for your specific operating system:

- [Installation on Red Hat Enterprise Linux (RHEL)](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-control-node-on-red-hat-enterprise-linux-rhel)
- [Installation on Ubuntu](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-control-node-on-ubuntu)
- [Installation on macOS](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-the-control-node-on-macos)

## Basic Usage

- To run a playbook, use the `ansible-playbook` command and specify the playbook file name:

```bash
ansible-playbook <playbook.yml>
```

- To execute a single task, you can use the `ansible` command and specify the task in the `--list-tasks` option:

```bash
ansible-playbook <playbook.yml> --list-tasks
```

## Inventory

Ansible uses an inventory file to manage the target hosts for automation. By default, the inventory file is located at `/etc/ansible/hosts`. You can specify a different inventory file using the `-i` option with the `ansible-playbook` command.

## Variables

Ansible supports variables, which can be used to store values for later use in playbooks. Variables can be defined in playbooks, inventory files, or in separate files. You can access the value of a variable using the syntax `{{ variable_name }}`.

## Modules

Ansible uses modules to perform various automation tasks, such as file and directory management, package installation, and service management. Some of the most commonly used modules include:

- `copy`: Copy files to the target host
- `file`: Manage files and directories on the target host
- `package`: Manage packages on the target host
- `service`: Manage services on the target host

You can find the complete list of Ansible modules in the [official documentation](https://docs.ansible.com/ansible/latest/modules/modules_by_category.html).

## Conclusion

Ansible is a powerful IT automation platform that helps you manage your infrastructure and applications with ease. With its simple syntax, inventory management, and support for variables and modules, Ansible makes it easy to automate complex tasks. This cheatsheet provides a brief overview of the most commonly used features in Ansible, but there is much more to explore in the official documentation.
