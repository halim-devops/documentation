## Examples

To use in local add 

Example of use in local add **ansible_user=wit ansible_password=witpassword** in the environment variables

To use on an ansible server
```
# to create account
ansible-playbook playbooks/userMongo.yml -e 'user=userToCreate password=changeme admin_password=adminPassword' --tags "create" -vvv

# to delete account
ansible-playbook playbooks/userMongo.yml -e 'user=userToDelete admin_password=adminPassword' --tags "delete" -vvv
```

> you may add following command line to specify which hosts file you are using
>```
>-i /home/wit/ansible/hosts
>```
>in `/etc/ansible/ansible.cfg` defaults hosts file is `/home/wit/ansibleops/hosts` which is **former hosts file**