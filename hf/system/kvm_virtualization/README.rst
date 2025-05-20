
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_kvm_virtualization
=====================
Setup Type 1 supervisor, Kvm virtualization on the target.
Thanks to https://www.youtube.com/watch?v=LHJhFW7_8EI
Thanks to https://sysguides.com/install-kvm-on-linux

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

Create file inventory with all your target servers
[servers]
192.168.0.26

Create file playbook_hf_nfs_server.yml with the list of export on the target servers

---
- hosts: servers
  become: true
  roles:
    - role: hf_kvm_virtualization
      vars:
        nfs_exports:
          - src: /mnt/b026_02/nfs_backup
            path: /mnt/nfsc
            folder: backup
            share: [192.168.0.0/24, 192.168.121.0/24]

Then run the command
❯ ansible-playbook -i ./inventory playbook_hf_nfs_server.yml --ask-become-pass

Check the result with
❯ showmount --exports 192.168.0.26
Export list for 192.168.0.26:
/mnt/b026_02/nfs_backup          192.168.121.0/24,192.168.0.0/24

License
-------
BSD, MIT

Author Information
------------------
This role was created in 2023 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
It is originally a fork of [Oefenweb/ansible-adminer](https://github.com/alainivars/ansible-roles/hf/authorized_keys).
