# Ansible role: sudo
Disable/lock root password,
create regular user with passwordless sudo privileges, 
copy ssh keys in for login to that user, and
set a random password, saved in ansible inventory host var.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `sudo_user` (default: `{{ ansible_user }}`): username of regular user with sudo privileges
+ `ssh_authorized_keys` (default: none): list of ssh pubkeys allowed to login
+ `pw_store` (default: `{{ inventory_dir }}/host_vars`):
  hashed passwords will be stored in subdirectories under this path,
  `{{ inventory_hostname }}/pw.yml`, in a key named `sudo_pw`

## Dependencies
None.

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
