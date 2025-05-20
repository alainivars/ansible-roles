
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.proxmox.group
================
Setup Proxmox server (work in progress).

hf.proxmox.group:
    - list groups
    - Add a new Proxmox group 'pve-admin'
    - Add a new Proxmox group 'pve-container'

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---

- name: Proxmox community
  hosts: all
  become: true
  roles:
     - roles/hf/system/proxmox/group

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
