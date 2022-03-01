Start roles

`/etc/ansible/playbooks/init.yaml`

```
---
- hosts: Containers
  gather_facts: yes
  vars_files:
    - /etc/ansible/roles/1-pre_jitsi/vars/main.yml                #lxc
    - /etc/ansible/roles/1-pre_jitsi/defaults/main.yml            #lxc
    - /etc/ansible/roles/2-Jitsi/defaults/main.yml                #jitsi
    - /etc/ansible/roles/2-Jitsi/vars/main.yml                    #jitsi

  roles:
    - role: "/etc/ansible/roles/1-pre_jitsi"
    - role: "/etc/ansible/roles/2-Jitsi"
```