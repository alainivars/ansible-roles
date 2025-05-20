
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_timezone
===========

Set timezone to.

Requirements
------------

None.

Role Variables
--------------

name: The user in the VM where you want o add the authorized key, default is 'vagrant'.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- hosts: "all"
  become: false
  roles:
    - { role: roles/hf/system/timezone, name: Etc/UTC }


License
-------

BSD, MIT

Author Information
------------------

This role was created in 2019 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
