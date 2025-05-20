
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.proxmox.user
===============
Setup Proxmox server (work in progress).

hf_proxmox.add_pam_user:
    - List Proxmox PAM user
    - Create a new Proxmox PAM user with group 'pve-admin' and 'pve-container'

Requirements
------------

None.

Role Variables
--------------

NEW_USER_NAME: new user name to be created on the target.
NEW_USER_PASSWORD: The new user password to connect to the UI

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
     - { role: roles/hf/proxmox/user }

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
