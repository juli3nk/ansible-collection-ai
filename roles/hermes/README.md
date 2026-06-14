OpenClaw
========

Install OpenClaw from npm as a specific Linux user.

This role installs the CLI only (no doctor, no onboarding, no systemd service management).
The target user must already exist and should be managed by the `identity` role.

Required variables
------------------

- `openclaw_user`
- `openclaw_npm_package`
- `openclaw_npm_version`

Example Playbook
----------------

    openclaw_user: john
    openclaw_group: john
    openclaw_npm_package: "openclaw"
    openclaw_npm_version: "latest"
    openclaw_npm_prefix: "/home/john/.npm-global"
    openclaw_npm_force_install: false

License
-------

MIT
