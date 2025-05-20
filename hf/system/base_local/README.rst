
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.system.base_local
====================

Install/Update locally all the Dependencies from Ansible Galaxy

Requirements
------------

None.

Role Variables
--------------

ansible_root: The default is /etc/ansible but on my personal system I install it in $HOME/.ansible
playbook_dir: The <place where you downloaded utils2devops>/ansible

Dependencies
------------

A lot of things.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- hosts: "all"
  become: false
  roles:
    - roles/hf/system/base_local



License
-------

BSD, MIT

Author Information
------------------

This role was created in 2019 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/). It is originally a fork of [Oefenweb/ansible-adminer](https://github.com/alainivars/ansible-roles/authorized_keys).
