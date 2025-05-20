
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.system.pci_passthrough
=========================
Setup pci passthrough (GPU).

pci_passthrough:
    - Check compatibility of the system
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

NEW_USER_NAME_LINUX: new user name to be created on the target.
PROXMOX_HOST: The Proxmox domain name or IP
PVE_NODE_NAME: The name of the pve we will create
PVE_ROOT_PASSWORD: The root password of the pve we will create
NEW_USER_PASSWORD: The new user password to connect to the UI
NEW_USER_TOKEN_ID: The new token ID (name)
NEW_USER_TOKEN_SECRET: The new secret like c97917ae-af85-4e4b-9997-4decd04f02f6

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
     - { role: roles/hf/system/pci_passthrough }

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
