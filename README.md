ANSIBLE
yum install epel-release
yum install ansible
yum install git
useradd -m ansible

useradd -m ansible
ansible ALL=(ALL) NOPASSWD: ALL

ansible server1 -m setup | less
ansible server1 -m ping

ansible server1 -b -m apt -a "update_cache=true name=apache2 state=present"
ansible server1 -b -m service -a "name=apache2 state=started"
ansible server1 -b -m service -a "name=apache2 state=stopped"

sudo su - ansible 
ssh-keygen
ssh-copy-id server.dominio.tld

ansible-playbook -i inv web.yml
ansible-playbook -i inv web.yml --check #dry-run

##variables
ansible-playbook -i inv web.yml -e "var1=value var2=value"

locate in file {{ var1 }}
