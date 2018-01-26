terminus_powerline
=========

Cross-platform ansible role for installation of Terminus font (patched with Powerline symbols)

Requirements
------------

One of the following OS (or deriviatives):
 - Debian
 - MacOS (with Homebrew)

Role Variables
--------------

    - terminus_powerline_env: system | user/users   # install font system-wide or user-wide
    - terminus_powerline_users:                     # list of users if running user-specific installation

Dependencies
------------

None

Example Playbook
----------------

    - hosts: dev_clients
      roles:
         - role: drew-kun.terminus_powerline

License
-------

MIT

Author Information
------------------

![Andrew Shagayev](drewshg@gmail.com)

