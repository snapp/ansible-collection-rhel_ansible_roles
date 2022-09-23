# repository_setup role

[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)

Please see the collection main page for a higher level description.

## Configuration

Below are the role default values from defaults/main.yml:

<pre>
---
# List of files to copy to /etc/yum.repos.d
# Available repository files in files/
repository_setup_repo_files_copy:
#  -

# List of files to remove in /etc/yum.repos.d
repository_setup_repo_files_remove:
#  -


# Configure or not Red Hat Subscription Management
repository_setup_rhsm_configure: true

# Install Satellite katello-ca-consumer-latest.rpm
# This will use the rhsm_baseurl variable defined below
repository_setup_install_katello_rpm: true

# Subscribe or unsubscribe to Red Hat or Satellite
repository_setup_rhsm_subscribe: true

# Red Hat Subscription Management parameters, see
# https://docs.ansible.com/ansible/latest/collections/community/general/redhat_subscription_module.html
# Leave activationkey and username undefined to skip RHSM configuration
repository_setup_rhsm_parameters:
  #activationkey:
  #org_id:

  #username:
  # This should come from vault
  #password:

  auto_attach: false
  #consumer_id:
  #consumer_name:
  #consumer_type:
  #environment:
  force_register: false
  #pool_ids:
  #  -
  #release:
  #rhsm_baseurl:
  #rhsm_repo_ca_cert:
  #server_hostname:
  #server_port:
  server_insecure: false
  #server_prefix:
  #server_proxy_hostname:
  #server_proxy_port:
  #server_proxy_user:
  #server_proxy_password:
  #syspurpose:


# List of Red Hat / Satellite repository IDs to disable
repository_setup_rhsm_repositories_disable:
#  -

# List of Red Hat / Satellite repository IDs to enable
repository_setup_rhsm_repositories_enable:
#  - rhel-{{ ansible_facts.distribution_major_version }}-for-x86_64-baseos-rpms
#  - rhel-{{ ansible_facts.distribution_major_version }}-for-x86_64-appstream-rpms

# Disable non-enabled Red Hat / Satellite repositories
repository_setup_rhsm_repositories_purge: true
</pre>

## License

GPLv3+