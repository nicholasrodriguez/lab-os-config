lab_os_config
=============

This role is used by this repo [https://github.com/nicholasrodriguez/lab] to ensure consistent base OS configuration for an Ansible lab or test environment and will perform the following:

 - Setup chrony
 - Detect if it is running on a VM and will install open-vm-tools
 - Setup the CentOS EPEL repo
 - Ensure firewalld is running
 - Update all the packages

Requirements
------------

Role tested on CentOS 7 and CentOS 8
- geerlingguy.ntp

Role Variables
--------------

| Variable                   | Default | Comments                                                                                                                                                  |
| :---                       | :---    | :---                                                                                                                                                      |
| `install_gui`    | `False`      | Will install a GUI if set to True|
| `ntp_enabled`    | -      | See geerlingguy.ntp|
| `ntp_package`    | -      | See geerlingguy.ntp|
| `ntp_area`    | -      | See geerlingguy.ntp|
| `ntp_manage_config`    | -      | See geerlingguy.ntp|
| `ntp_servers`    | -      | See geerlingguy.ntp|
| `-`    | -      | -                                      |


Dependencies
------------

None required


Example Playbook
----------------

```
    - hosts: servers
      roles:
         - role: nicholasrodriguez.lab_os_config
```
License
-------

MIT

Author Information
------------------

- https://github.com/nicholasrodriguez/ (maintainer)
