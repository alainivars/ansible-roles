
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_nfs_server
=============
Setup a NFS server on the target.

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
    - role: hf_nfs_server
      vars:
        nfs_exports:
          - src: /mnt/b026_02/nfs_backup
            path: /mnt/nfsc
            folder: backup
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_document
            path: /mnt/nfsc
            folder: document
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_photos
            path: /mnt/nfsc
            folder: photos
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_videos
            path: /mnt/nfsc
            folder: videos
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_musics
            path: /mnt/nfsc
            folder: musics
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_highfeature
            path: /mnt/nfsc
            folder: highfeature
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_hf_kubernetes
            path: /mnt/nfsc
            folder: hf_kubernetes
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_hf_docker
            path: /mnt/nfsc
            folder: hf_docker
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_hf_vms
            path: /mnt/nfsc
            folder: hf_vms
            share: [192.168.0.0/24, 192.168.121.0/24]
          - src: /mnt/b026_02/nfs_hf_repositories
            path: /mnt/nfsc
            folder: hf_repositories
            share: [192.168.0.0/24, 192.168.121.0/24]

Then run the command
❯ ansible-playbook -i ./inventory playbook_hf_nfs_server.yml --ask-become-pass

Check the result with
❯ showmount --exports 192.168.0.26
Export list for 192.168.0.26:
/mnt/b026_02/nfs_hf_repositories 192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_hf_vms          192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_hf_docker       192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_hf_kubernetes   192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_highfeature     192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_musics          192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_videos          192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_photos          192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_document        192.168.121.0/24,192.168.0.0/24
/mnt/b026_02/nfs_backup          192.168.121.0/24,192.168.0.0/24

License
-------
BSD, MIT

Author Information
------------------
This role was created in 2023 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
It is originally a fork of [Oefenweb/ansible-adminer](https://github.com/alainivars/ansible-roles/hf/authorized_keys).
