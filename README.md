# Nat's dotfiles

## Synopsis

Applies my preferred environment to a workstation.

## Requirements

- [Ansible](https://www.ansible.com/) >= 2.4.0.0
- [Arch Linux](https://www.archlinux.org/) or MacOS + [Homebrew](https://brew.sh/)
    - Should be easily forked & ported to other Linux distributions by just tweaking package names

## Running

There are two playbooks - 1 for package installation and another for user-level settings.

### Common

    $ git clone https://github.com/nharward/dotfiles.git
    $ cd dotfiles/ansible

### Package

Run as the `root` user on Linux, or pass in `--ask-become-pass` as an argument to `ansible-playbook` if not root

    $ ansible-playbook -i inventory packages.yml

### User level settings

    $ ansible-playbook -i inventory user.yml
