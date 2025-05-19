
.. image:: https://api.travis-ci.org/alainivars/ansible-roles.svg?branch=master
    :target: http://travis-ci.org/alainivars/ansible-role
    :alt: Build status

hf_provision_system
===================

Provision system by:

    - Check when apt was last updated
    - Update apt repo and cache on all Debian/Ubuntu boxes
    - Upgrade all packages on server
    - Autoremove Un-used package
    - Reboot if required

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

Including an example of how to use your role:

---
 - hosts: all
   become: false
   roles:
     - hf_provision_system

License
-------

BSD, MIT

Author Information
------------------

This role was created in 2019 by [Alain Ivars](https://www.linkedin.com/in/ivarsalain/).
