[![CI](https://github.com/de-it-krachten/ansible-role-lvm/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lvm/actions?query=workflow%3ACI)


# ansible-role-lvm

Sets up LVM (Logical volume managment)<br>
Create volume groups, logical volume & file systems

Platforms
--------------

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- CentOS 7
- RockyLinux 8
- AlmaLinux 8<sup>1</sup>
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS

Note:
<sup>1</sup> means no automated testing is performed on these platforms

Role Variables
--------------
<pre><code>
# List of required packages
lvm_packages:
  - lvm2

# Defaults lists of volumegroups, logical volumes and file systems
lvm:
  vg: []
  lv: []
  fs: []

# Shrink logical volumes
lvm_shrink: false

# Resize file system after logical volume changes
lvm_resizefs: true
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
