# cisco_compliance

cisco compliance reporting

Include these values to have emails sent. Can be included as extra vars or in a vars file.

```
email_address:
from_email:
smtp_server:
```

vars used in jinja2 templates:

```
management_interface:
ntp_address:
logging_address:
    - dest 1
    - dest 2
snmp_ro:
enable_pass:
local_user:
local_pass:
domain_name:
syslog_server:
protect_snmp_var:
    - acl 1
    - acl 2
```
