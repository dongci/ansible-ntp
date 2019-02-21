ansible-ntp:
------------------------------------------------------
1> Edit the ./inventory/hosts configuration file

```
[ntpser]
10.0.0.101

[ntpclt]
10.0.0.102
10.0.0.103

[ntp:children]
ntpser
ntpclt

[ntp:vars]
ntp_server=cn.pool.ntp.org
ntp_network=10.0.0.0/24
ntp_client_server=10.0.0.101
```

2> Install base
```
ansible-playbook site.yml --tags ntp
```

------------------------------------------------------
