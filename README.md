# ansible-role-flatpak
![License](https://img.shields.io/github/license/jamescherti/ansible-role-flatpak)

The `ansible-role-flatpak` Ansible role installs and configures Flatpak, adds Flathub as a remote repository, and optionally manages Flatpak packages and updates. This role supports specific Linux distributions: Debian-based, Gentoo, and Arch Linux.

## Requirements

- Supported operating systems: Debian/Ubuntu (and their derivatives), Gentoo, Arch Linux.
- Ansible
- Ansible collections:
  - `community.general`

## Role Variables

The following variables can be set to customize the role's behavior:

| Variable                   | Description                                                                                         | Default       |
|----------------------------|-----------------------------------------------------------------------------------------------------|---------------|
| `flatpak_proxy`            | Proxy settings for Flatpak (optional). Leave empty if not using a proxy.                           | `""`          |
| `flatpak_packages`         | List of Flatpak packages to install from Flathub.                                                  | `[]`          |
| `flatpak_auto_update`      | Whether to enable automatic daily updates and cleanup of Flatpak packages.                         | `false`       |
| `flatpak_auto_update_cmd_prefix` | Optional prefix command to run before the Flatpak update command (e.g., `nice`, `ionice`).    | Not defined   |
| `flatpak_auto_update_cmd_suffix` | Optional suffix to append to the Flatpak update command.                                      | Not defined   |

## Author and license

Copyright (C) 2025 [James Cherti](https://www.jamescherti.com).

Distributed under terms of the MIT license.

# Links

- [ansible-role-flatpak @GitHub](https://github.com/jamescherti/ansible-role-flatpak)
