Cursor CLI
==========

Install Cursor CLI as a specific Linux user.

This role installs the CLI only (no authentication/login workflow, no systemd service management).
The target user must already exist and should be managed by the `identity` role.

Prerequisites
-------------

- `curl` and `ca-certificates` must be installed before this role runs.
- Package installation is intentionally delegated to the `system.package` role.

Required variables
------------------

- `cursor_cli_user`
- `cursor_cli_binary_path`
- `cursor_cli_install_script_url`

Example Playbook
----------------

    cursor_cli_user: openclaw
    cursor_cli_binary_path: /home/openclaw/.local/bin/agent
    cursor_cli_install_script_url: https://cursor.com/install
    cursor_cli_prerequisite_packages:
      - curl
      - ca-certificates
    cursor_cli_force_install: false

License
-------

MIT
