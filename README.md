Ansible role: terminus_powerline
=========

[![MIT licensed][mit-badge]][mit-link]
[![Galaxy Role][role-badge]][galaxy-link]

Cross-platform ansible role for System-wide installation of Terminus font (patched with Powerline symbols)

Requirements
------------

NOTE: Role requires Fact Gathering by ansible!

One of the following OS (or deriviatives):
 - Debian
 - MacOS (with [Homebrew][homebrew])

For MacOS:
if Homebrew is not installed on the managed host, install the following role via galaxy:

    ansible-galaxy install drew_kun.homebrew

 And include it in the playbook:

    roles:
        - drew_kun.homebrew

Role Variables
--------------

OS-Specific:

| Variable | Description | Default |
|----------|-------------|---------|
| **terminus_powerline_fonts_dir** | Directory where the fonts being installed | <ul><li>Darwin: `/Library/Fonts/`</li><li>Debian: `/usr/local/share/fonts`</li></ul> |

Dependencies
------------

None

Example Playbook
----------------

For MacOS:

    - hosts: dev_clients_macos
      gather_facts: yes
      roles:
        - drew_kun.homebrew
        - drew_kun.terminus_powerline

For Linux:

    - hosts: dev_clients_linux
      gather_facts: yes
      roles:
        - drew_kun.terminus_powerline

License
-------

[MIT][mit-link]

Author Information
------------------

Andrew Shagayev

[role-badge]:https://img.shields.io/badge/role-drew__kun.terminus__powerline-green.svg
[galaxy-link]: https://galaxy.ansible.com/drew_kun/terminus_powerline/
[mit-badge]: https://img.shields.io/badge/license-MIT-blue.svg
[mit-link]: https://raw.githubusercontent.com/drew_kun/ansible-terminus_powerline/master/LICENSE
[homebrew]: http://brew.sh/
