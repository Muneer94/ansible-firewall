# Ansible Role: Deploy Firewall
===============================

Install and configure ufw

## Role Variables
-----------------

### UFW install configuration
-----------------------------

```
ufw_packages:
  - ufw

```

### UFW basic configuration
---------------------------

```
ufw_ipv6: "yes"
ufw_default_input_policy: DROP
ufw_default_output_policy: ACCEPT
ufw_default_forward_policy: DROP
ufw_logging: "off"

```

### UFW service configuration
-----------------------------

```
ufw_state: enabled
ufw_reset: yes

```

### UFW custom configuration
----------------------------

```
ufw_rules: [{ port: 22, rule: allow }]

```

### Example Playbook
--------------------

```
    - hosts: servers
      roles:
         - deploy.firewall
```
