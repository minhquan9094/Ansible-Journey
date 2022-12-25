# Lab Guideline


### Ansible working with Windows using winrm
- Using this command to running win_ping to testing connection from ansible to Winserver

```
# inventory file:

[winsrv]
192.168.92.225
10.10.137.14
192.168.92.220
10.10.137.8
10.10.137.13


[winsrv:vars]
ansible_user=
ansible_password=
ansible_port=5985
ansible_connection=winrm
ansible_winrm_transport=ntlm
#ansible_winrm_server_cert_validation=ignore
#ansible_winrm_scheme=http
#ansible_become_method=runas
#ansible_become_user=SYSTEM

```


```
Running command
ansible all -i inventory -m win_ping
```


