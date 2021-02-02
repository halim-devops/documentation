## Examples

To use in local add 

Example of use in local add **ansible_user=wit ansible_password=witpassword** in the environment variables

```
# deploy conf
ansible-playbook playbooks/screenshot.yml -e 'hosts=batch-server' --tags "conf" -vvv

# deploy jar
ansible-playbook playbooks/screenshot.yml -e 'jar_version=jarVersion hosts=batch-server' --tags 'jar' -vvv

# restart screenshot services
ansible-playbook playbooks/screenshot.yml -e 'hosts=puppeteer_server' --tags='redeploy-screenshots' -vvv

# update screenshot services version and restart
ansible-playbook playbooks/screenshot.yml -e 'hosts=puppeteer_server' --tags='update-screenshots' -vvv

# deploy haproxy configuration
ansible-playbook playbooks/screenshot.yml -e 'hosts=puppeteer_haproxy' --tags='deploy_haproxy_conf' -vvv

```

> you may add following command line to specify which hosts file you are using
>```
>-i /home/wit/ansible/hosts
>```
>in `/etc/ansible/ansible.cfg` defaults hosts file is `/home/wit/ansibleops/hosts` which is **former hosts file**