
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_nfs_client
=============
Setup a NFS client on the target, and add to fstab all the entries.

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

Create file inventory with all your target clients
[clients]
192.168.0.16

Create file playbook.yml with the list of export on the target servers

---
- hosts: clients
  become: true
  roles:
    - roles/hf/system/nfs/client
  vars:
    nfsmounts:
      - src: 192.168.0.26:/mnt/b026_02/nfs_backup
        path: /mnt/nfsc_backup
        owner: a
        group: a
      - src: 192.168.0.26:/mnt/b026_02/nfs_document
        path: /mnt/nfsc_document
        owner: a
        group: a


Then run the command
❯ ansible-playbook -i ./inventory playbook.yml --ask-become-pass

License
-------
BSD, MIT

Author Information
------------------
This role was created in 2023 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
It is originally a fork of [Oefenweb/ansible-adminer](https://github.com/alainivars/ansible-roles/hf/authorized_keys).
