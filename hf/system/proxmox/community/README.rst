
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.proxmox.community
====================
Setup Proxmox server (work in progress).

hf.proxmox.community:
    - Disable Proxmox subscription popup
    - Modify sources.list to use pve-no-subscription repository (Proxmox 8.*)
    - Remove pve-enterprise repository if exists
    - Update apt cache
    - Perform a dist-upgrade
    - Check if reboot is required
    - Reboot the server if required
    - Remove not required dependencies

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
     - roles/hf/system/proxmox/community

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
