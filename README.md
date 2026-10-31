# ansible
Ansible for Home Lab

## How to run the playbook
Check available playbooks on `playbooks` directory.

Change `name_of_playbook` to available playbook that you want to run, for example:
```
- import_playbook: "playbooks/<name_of_playbook>.yaml"
```
Bellow `playbook`, we have a mandatory variable `vars`. `hosts`, it contain specific host that you want to run on. You can check on `inventory/inventory.yaml` for available hosts. You can also use `all` if you want to run the playbook to all available hosts.

For playbook that run roles, you can check available variables on every role. Example playbook for running `sshd` role
```
---
- import_playbook: "{{ ANSIBLE_WORKSPACE }}/playbook/sshd.yaml"
  vars:
    hosts: all
    sshd_port: 2209
```

Then commit your changes.

## Docs
For Ansible Docs, you can check it on here https://github.com/Playground-Server/docs/blob/main/tools_ansible.md