
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_proxmox
==========
Setup Proxmox server (work in progress).

hf_proxmox:
    - Update repository cache
    - Install proxmoxer
    - Check if a token for a user
    - Display user Information
    - Create a token for a user
    - Display user Information

hf_proxmox.add_pam_user:
    - Add a new Proxmox PAM user

hf_proxmox.community:
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
  tasks:
    - name: Run tasks/community.yaml instead of 'main'
      ansible.builtin.include_role:
        name: community role
        tasks_from: community

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
