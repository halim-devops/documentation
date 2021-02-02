## Examples

To use in local add 

Example of use in local add **ansible_user=wit ansible_password=witpassword** in the environment variables

To use on an ansible server

```
# deploy service conf
ansible-playbook playbooks/w2p.yml -e 'hosts=prwv4' --tags "service_conf_deploy" -vvv

# deploy conf
ansible-playbook playbooks/w2p.yml -e 'hosts=prwv4' --tags "conf,logback.xml,workit.functional.properties,workit.datasources.properties" -vvv
```

> you may add following command line to specify which hosts file you are using
>```
>-i /home/wit/ansible/hosts
>```
>in `/etc/ansible/ansible.cfg` defaults hosts file is `/home/wit/ansibleops/hosts` which is **former hosts file**