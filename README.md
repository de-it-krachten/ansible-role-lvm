[![CI](https://github.com/de-it-krachten/ansible-role-lvm/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lvm/actions?query=workflow%3ACI)


# ansible-role-lvm

Sets up LVM (Logical volume managment)<br>
Create volume groups, logical volume & file systems

Platforms
--------------

Supported platforms

- CentOS 7
- RockyLinux 8
- AlmaLinux 8
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS



Role Variables
--------------
<pre><code>
lvm_packages:
  - lvm2

lvm:
  vg: []
  lv: []
  fs: []
</pre></code>


Example Playbook
----------------

<pre><code>
- name: sample playbook for role 'lvm'
  hosts: all
  vars:
  tasks:
    - name: Include role 'lvm'
      include_role:
        name: lvm
</pre></code>
