
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_authorized_keys
==================

Set authorized key for user 'user' copying it from current user.

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

---
 - hosts: all
   become: false
   roles:
     - hf_authorized_keys

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2019 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
It is originally a fork of [Oefenweb/ansible-adminer](https://github.com/alainivars/ansible-roles/hf/authorized_keys).
