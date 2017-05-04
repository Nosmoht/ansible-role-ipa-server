ipa_server
=========
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Variables](#variables)
- [Tags](#tags)
- [Usage](#usage)
- [Author](#author)

# Introduction
Install and configure IPA server.

# Requirements


# Variables
| Name | Description | Default |
|:-----|:------------|:--------|
| ipa_server_package_names | List of packages to ensure | ? |
| ipa_server_package_state | Package state | installed |
| ipa_server_service_names | List of service name | ? |
| ipa_server_service_state | Service state | running |
| ipa_server_service_enabled | Service enabled | true |
| ipa_server_flush_handlers | Boolean to define if all handlers should be flushed | true |
| ipa_server_realm_name | Realm name | EXAMPLE.COM |
| ipa_server_domain_name | Domain name | example.com |
| ipa_server_directory_manager_password | Directory manager password | t0ps3cr3t |
| ipa_server_admin_user | Administrative user name | admin |
| ipa_server_admin_password | Administrative user password | t0ps3cr3t |
| ipa_server_hostname | IPA Server hostname | '{{ ansible_nodename }}' |
| ipa_server_ip_address | IPA Server ip address | '{{ ansible_eth0.ipv4.address }}' |
| ipa_server_mkhomedir | Create home directories | true |
| ipa_server_setup_dns | Setup DNS server | false |
| ipa_server_ssh_trust_dns | ? | false |
| ipa_server_hbac_allow | Allow HBAC | true |
| ipa_server_setup_ntp | Secure NTP | true |
| ipa_server_configure_ssh | Configure SSH | true |
| ipa_server_configure_sshd | Configure SSHD | true |
| ipa_server_ui_redirect | Redirect UI | true |

# Tags
- ipa_server_install: ensure that all packages in __ipa_server_package_names__ are in state __ipa_server_package_state__
- ipa_server_config: ensure configuration
- ipa_server_service: ensure that all services in __ipa_server_service_names__ are in state __ipa_server_service_state__

# Usage

Example playbook

```yaml
- hosts: 127.0.0.1
  roles:
  - role: ipa_server
```

# Author
[Thomas Krahn](mailto:thomas.krahn@esailors.de)
