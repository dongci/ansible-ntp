ansible-ntp:
------------------------------------------------------
1> Edit the ./inventory/hosts configuration file

```
ntp_server=cn.pool.ntp.org
ntp_network=10.0.0.0/24
ntp_client_server=10.0.0.101
```

2> Install base
```
ansible-playbook site.yml --tags ntp
```

------------------------------------------------------
