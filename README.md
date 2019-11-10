# Ansible role: sudo
Allow regular user to use sudo without password.
User should exist already and be secured
(e.g., with disabled password and only SSH pubkey login)

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `sudo_user` (default: `{{ ansible_user }}`): username of regular user with sudo privileges

## Dependencies
None

## Example Playbook

```
- hosts: all
  roles:
    - { role: ho-ansible.sudo }
```

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
