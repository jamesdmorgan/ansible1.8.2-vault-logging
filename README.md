# ansible1.8.2-vault-logging
Issue with Ansible vault logging senstive information

ansible-playbook site.yml -v

```yaml
PLAY [localhost] ************************************************************** 

GATHERING FACTS *************************************************************** 
ok: [localhost]

TASK: [vault-test | include_vars sensitive.yml] ******************************* 
ok: [localhost] => {"ansible_facts": {"sensitive_data": "-----BEGIN RSA PRIVATE KEY-----\nMIIEogIBAAKCAQEAtFEdPhLNSzdrVv2R1nFeMuCFMce9JiJoaz7DdbB6dZcUnSHh\n.... THIS SHOULD NOT BE LOGGED\nT+/LAoGAGGRqce3XZ54G4nwYMEZxSPqpl0xh3quGrP7CH/VMOWat6DUbURiUJkcA\nmDjHVx35Y2fyv+LpGrPeVFt+s65N/wkJV4S+671gXV9K0YTB9PGKRf96AksjOlqg\n+gqMdXuuWjXTCg6ps7uKilfxDhkyCzB0NUVy2ngYvaLuoEN+/AM=\n-----END RSA PRIVATE KEY-----"}}

PLAY RECAP ******************************************************************** 
localhost                  : ok=2    changed=0    unreachable=0    failed=0   
```
