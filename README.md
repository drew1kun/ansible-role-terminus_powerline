terminus_powerline
=========

Cross-platform ansible role for installation of Terminus font (patched with Powerline symbols)

Requirements
------------

One of the following OS (or deriviatives):
 - Debian
 - MacOS (with [Homebrew][homebrew])

For MacOS:
if Homebrew is not installed on the managed host, install the following role via galaxy:

    ansible-galaxy install drew-kun.homebrew

 And include it in the playbook:

    roles:
        - drew-kun.homebrew

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
        - drew-kun.homebrew
        - drew-kun.terminus_powerline

License
-------

[MIT][mit-link]

Author Information
------------------

![Andrew Shagayev](drewshg@gmail.com)

[role-badge]:https://img.shields.io/badge/role-drew--kun.terminus__powerline-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew-kun/terminus_powerline/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/geerlingguy/ansible-role-homebrew/master/LICENSE
[homebrew]: http://brew.sh/
