
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf.system.user_key.add
======================

Get existing users
Create new user with no password with OpenSSH keypair (4096 bits, RSA)

Requirements
------------

None.

Role Variables
--------------

NEW_USER_NAME_LINUX: new user name to be created on the target.

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
     - roles/hf/system/user_key/create

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2025 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/)
