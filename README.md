Ansible role: terminus_powerline
=========

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Cross-platform ansible role for installation of [Terminus font][terminus-git] (patched with [Powerline][powerline-git] symbols)

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

OS-Agnostic:

    terminus_powerline_env: system | user/users     # install font system-wide or user-wide
    # Attention: On MacOS font always will be installed system-wide

    terminus_powerline_users:                       # list of users if running user-specific installation

OS-Specific:

    terminus_powerline_fonts_dir:                   # directory where the fonts being installed

Dependencies
------------

None

Example Playbook
----------------

For MacOS:

    - hosts: dev_clients_macos
      roles:
        - drew-kun.homebrew
        - drew-kun.terminus_powerline

For Linux:

    - hosts: dev_clients_linux
      roles:
        - drew.kun.terminus_powerline

License
-------

[MIT][mit-link]

Author Information
------------------

Andrew Shagayev

[role-badge]:https://img.shields.io/badge/role-drew--kun.terminus__powerline-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew-kun/terminus_powerline/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew-kun/ansible-terminus_powerline/master/LICENSE
[homebrew]: http://brew.sh/
[terminus-git]: https://github.com/drew-kun/terminus_powerline_font_osx
[powerline-git]: https://github.com/powerline/fonts
