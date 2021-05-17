lab_os_config
=============

This role is used by the following repo to ensure consistant base OS configuration for an Ansible lab or test environment

[https://github.com/nicholasrodriguez/lab]

Requirements
------------

Role tested on CentOS 7 and CentOS 8
- geerlingguy.ntp

Role Variables
--------------

| Variable                   | Default | Comments                                                                                                                                                  |
| :---                       | :---    | :---                                                                                                                                                      |
| `ntp1`    | -      | First NTP source for chrony configuration.                                      |
| `ntp2`    | -      | Second NTP source for chrony configuration.                                      |

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
