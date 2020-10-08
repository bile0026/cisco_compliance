# cisco_compliance

cisco compliance reporting

# Current Issues

- Need to do testing with TACACS and password settings (hashed secrets)
- No template for 9300 or 9500 switches

Include these values to have emails sent. Can be included as extra vars or in a vars file.

```
email_address:
from_email:
smtp_server:
```

vars used in jinja2 templates (see examples in vars/vars.yml):

```
management_interface: GigabitEthernet0/0
ntp_address: 192.168.0.1
snmp_ro: public
enable_pass: cisco
local_user: cisco
local_pass: cisco
domain_name: test.com
syslog_server:
  - 192.168.0.1
  - 192.168.1.1
protect_snmp_var:
  - permit 192.168.0.1
  - permit 192.168.0.2
  - deny   any log
tacacs_key: 12345678
tacacs_server_name:
  - name: server 1
    ip: 192.168.0.1
  - name: server 2
    ip: 192.168.1.1
banner: |
  UNAUTHORIZED ACCESS TO THIS DEVICE IS PROHIBITED
  ================================================
  You must have explicit authorized permission to access or
  configure this device. Unauthorized attempts and actions to access or use this
  system may result in civil and/or criminal penalties. All activities performed
  on this device are monitored and logged.
  ================================================
```

To get email reports, include these variables:

```
email_addresses:
    - email@example.com
from_email: email@example.com
smtp_server: email.example.com
```
