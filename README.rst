
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

ansible-roles
=============
Some useful Ansible roles in use in utils2devops library

Role list::

    hf/system/base_local : Install/Update locally all the Dependencies from Ansible Galaxy
    hf/system/authorized_keys : Set authorized key for user 'user' copying it from current user.
    hf/system/packet_management: Provision system.
    hf/system/nfs/client : Setup a NFS client on the target, and add to fstab all the entries.
    hf/system/nfs/server : Setup a NFS server on the target.
    hf/system/proxmox/community : Setup Proxmox server (work in progress).
    hf/system/proxmox/group : Setup Proxmox server (work in progress).
    hf/system/proxmox/token : Setup Proxmox server (work in progress).
    hf/system/proxmox/user : Setup Proxmox server (work in progress).
    hf/system/service/clean : Check Service, stop and Delete Service.
    hf/system/service/setup : Setup Service.
    hf/system/service/start : Reload and Start Service.
    hf/system/timezone : Set timezone to.
    hf/system/user_key/add : Add my key if not exists in authorized_keys
    hf/system/user_key/authorized_keys : Add a key if not exists in authorized_keys
    hf/system/user_key/create : Create new user with no password with OpenSSH keypair (4096 bits, RSA)

