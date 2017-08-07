ansible-role-tigervnc
=========

Install and configure TigerVNC for one user.

Requirements
------------

None

Role Variables
--------------

Name               | Required | Default                     | Comment
---                | ---      | ---                         | ---
tigervnc_user      | yes      | none                        | Already existing user to setup VNC for
tigervnc_vncpass   | yes      | none                        | VNC password
tigervnc_user_home | yes      | `/home/{{ tigervnc_user }}` | The user home directory


Example Playbook
----------------

```yaml
---
- name: Test play
  hosts: all
  become: true
  gather_facts: true
  vars:
    tigervnc_user: vagrant
    tigervnc_vncpass: test1
  roles:
    - role: ansible-role-tigervnc
```
