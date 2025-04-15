# ansible-role-flatpak
![License](https://img.shields.io/github/license/jamescherti/ansible-role-flatpak)

The *ansible-role-flatpak* Ansible role installs and configures Flatpak, adds Flathub as a remote repository, and optionally manages Flatpak packages and updates. This role supports specific Linux distributions: Debian-based, Gentoo, and Arch Linux.

## Requirements

- Supported operating systems: Debian/Ubuntu (and their derivatives), Gentoo, or Arch Linux.
- Ansible collections:
  - community.general

## Role Variables

The following variables can be set to customize the role's behavior:

| Variable                              | Description                                                                                                                                  | Default                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| `flatpak_packages`                    | List of Flatpak packages to install.                                                                                                         | []                               |
| `flatpak_update_script`               | Whether to enable automatic daily updates and cleanup of Flatpak packages.                                                                   | false                            |
| `flatpak_update_script_cmd_prefix`    | Optional prefix command to run before the Flatpak update command (e.g., `nice`, `ionice`).                                                   | ''                               |
| `flatpak_update_script_cmd_suffix`    | Optional suffix to append to the Flatpak update command.                                                                                     | '>/dev/null'                     |
| `flatpak_update_script_remove_unused` | Delete unused Flatpak packages after a successful update                                                                                     | true                             |
| `flatpak_update_script_script_path`   | Path to the update script.                                                                                                                   | '/etc/cron.daily/flatpak-update' |
| `flatpak_install_desktop_portal`      | Install the desktop portal. Values: '' (no desktop portal), "gtk", or "gnome". Can be a string or a list of values, such as ["gtk", "gnome"] | ['gtk']                          |
| `flatpak_proxy`                       | Proxy settings for Flatpak (optional). Leave empty if not using a proxy.                                                                     | ''                               |

## Author and license

The *ansible-role-flatpak* role has been written by [James Cherti](https://www.jamescherti.com/) and is distributed under terms of the MIT license.

Copyright (C) 2025 James Cherti

Distributed under terms of the MIT license.

# Links

- [ansible-role-flatpak @GitHub](https://github.com/jamescherti/ansible-role-flatpak)
