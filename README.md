[![CI](https://github.com/de-it-krachten/ansible-role-lvm/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-lvm/actions?query=workflow%3ACI)


# ansible-role-lvm

Sets up LVM (Logical volume managment)<br>
Create volume groups, logical volume & file systems


## Dependencies

#### Roles
None

#### Collections
- community.general
- ansible.posix

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 10 (Buster)<sup>1</sup>
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 37
- Fedora 38

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
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




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'lvm'
  hosts: all
  become: "yes"
  tasks:
    - name: Include role 'lvm'
      ansible.builtin.include_role:
        name: lvm
</pre></code>
