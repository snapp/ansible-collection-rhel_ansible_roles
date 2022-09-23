# boot_parameters role

[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)

Please see the collection main page for a higher level description.

## Configuration

Below are the role default values from defaults/main.yml:

<pre>
---
boot_parameters_enable:
  - quiet

boot_parameters_disable:
  - debug
  - rhgb

boot_parameters_timeout: 1

# Protect boot parameters with password
# NB. For the time being this should be
# PBKDF2 hash to allow idempotency, use
# grub2-mkpasswd-pbkdf2(3) to create one
# Boot loader username is always 'root'
# This should come from vault
#boot_parameters_password:

# Reboot system after parameter changes
boot_parameters_reboot: true
</pre>

## License

GPLv3+