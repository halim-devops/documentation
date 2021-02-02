## Examples

To use in local add 

Example of use in local add **ansible_user=wit ansible_password=witpassword** in the environment variables

To use on an ansible server
```
# deploy exporter jar 
ansible-playbook playbooks/exporter.yml -e 'jar_version=1.8.266' --tags='jar' -vvvv

```

> you may add following command line to specify which hosts file you are using
>```
>-i /home/wit/ansible/hosts
>```
>in `/etc/ansible/ansible.cfg` defaults hosts file is `/home/wit/ansibleops/hosts` which is **former hosts file**