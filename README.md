nicenemo.debianbase
=========
> WARNING: work in progress
Base Installation of a Debian system.
Sets local mirrors, updates packages, install/remove lists of packages. Add users with sudo rights.

Requirements
------------

Any installed Debian or Debian derivate, e.g. Raspberry Pi OS Ubuntu.
Only tested with Debian and Raspberry Pi-OS.


Role Variables
--------------

* `packages_to_add`
* `packages_to_remove`
* `users_to_delete`


Dependencies
------------

None

Example Playbook
----------------


```
#!ansible-playbook
---
- name: Configure debian_servers.
  hosts: debian_servers
  become: true
  roles:
    - nicenemo.debianbase
```

Note that for now it assumes a folder `authorized_keys` next to your playbook. The `authorized_keys` folder  contains the public keys of the users with sudo rights.
Each file is named the same as the username.

> This will likely change.


Future Changes
--------------

Add a second list of packages to install, e.g. for firmware
Do user creation from a list in  the inventory file instead of everything in authorized_keys.

License
-------

MIT

Author Information
------------------
 [Hans Kruse](https://www.hanskruse.eu)
