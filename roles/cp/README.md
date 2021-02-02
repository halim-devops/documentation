## Examples

To use in local add 

Example of use in local add **ansible_user=wit ansible_password=witpassword** in the environment variables

To use on an ansible server
```
# deploy conf on qa back servers
ansible-playbook playbooks/cp.yml -e 'hosts=cp_back_qa' --tags='conf' -vvvv

# deploy jar on qa back servers
ansible-playbook playbooks/cp.yml -e 'hosts=admin-services_qa jar_version=1.32.0' --tags='jar' -vvvv

# restart components
ansible-playbook playbooks/cp.yml -e 'hosts=admin-cp_qa' --tags='restart' -vvvv

# deploy jar on specified back servers
ansible-playbook playbooks/cp.yml -e 'hosts=admin-services_qa,manager_qa,processor_qa,warning_qa,stats-builder_qa,offer-adaptor_qa jar_version=1.33.0' --tags='jar' -vvvv

```

> you may add following command line to specify which hosts file you are using
>```
>-i /home/wit/ansible/hosts
>```
>in `/etc/ansible/ansible.cfg` defaults hosts file is `/home/wit/ansibleops/hosts` which is **former hosts file**