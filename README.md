# cisco_compliance

cisco compliance reporting

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
```

To get email reports, include these variables:

```
email_addresses:
    - email@example.com
from_email: email@example.com
smtp_server: email.example.com
```
