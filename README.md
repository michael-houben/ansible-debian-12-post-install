# ansible-debian-12-post-install

[![Actively Maintained](https://img.shields.io/badge/Maintenance%20Level-Actively%20Maintained-green.svg)](https://gist.github.com/cheerfulstoic/d107229326a01ff0f333a1d3476e068d)

Installs some essential packages and applies some basic configurations.

## Requirements
Requires Ansible 2.10 or later. This role has only been tested on Debian 12 (Bookworm).

## Role Variables
Please edit at least all variables with  `__edit_me__` placeholder in [`defaults/main.yml`](https://github.com/michael-houben/ansible-debian-12-post-install/blob/main/defaults/main.yml). A list of packages for installation is defined in the same file.

## Dependencies
None

## Example Playbook

    - hosts: all
      become: yes
      become_method: sudo
      roles:
        - ansible-debian-12-post-install

## Example Inventory

*inventory.yml*

    ---
    servers:
      hosts:
        192.168.0.11:
          ansible_ssh_user: admin
          machine_hostname: server01
        192.168.0.12:
          ansible_ssh_user: admin
          machine_hostname: server02
        192.168.0.13:
          ansible_ssh_user: admin
          machine_hostname: server03

## License
GPL-3.0 License

## Author Information
This role was created by Michael Houben, based on <https://github.com/dan-kir/ansible-debian-11-post-install> by Dan Kir
