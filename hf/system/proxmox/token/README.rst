
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.proxmox.token
================
Setup Proxmox server (work in progress).

hf.proxmox.token:
    - Update repository cache
    - Install proxmoxer
    - Check if a token for a user
    - Display user Information
    - Create a token for a user
    - Display user Information

Requirements
------------

None.

Role Variables
--------------

NEW_USER_NAME: new user name to be created on the target.
NEW_USER_TOKEN_ID: The new token ID (name)

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
     - { role: roles/hf/proxmox/token }

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
