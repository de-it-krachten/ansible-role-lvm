[![CI](https://github.com/de-it-krachten/ansible-role-lvm/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lvm/actions?query=workflow%3ACI)


# ansible-role-lvm

Sets up LVM (Logical volume managment)<br>
Create volume groups, logical volume & file systems


Platforms
--------------

Supported platforms

- CentOS 7
- CentOS 8
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
</pre></code>


Example Playbook
----------------

<pre><code>
- name: Converge
  hosts: all
  vars:
    lvm:
      vg:
        - name: vg01
          pv: /dev/sdb
      lv:
        - name: lv01
          vg: vg01
          size: 1G
          mp: /mnt/lv01
          fstype: ext4

  tasks:
    - name: Include role 'ansible-role-lvm'
      include_role:
        name: ansible-role-lvm
</pre></code>
