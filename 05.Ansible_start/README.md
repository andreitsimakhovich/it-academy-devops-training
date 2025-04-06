## Homework Assignment 1: Setting Up Ansible

### Ansible installation
1. Install pip - ```sudo apt install python3-pip```
2. Install ansible - ```pip3 install --user ansible```
3. Check installation - ```ansible --version``` 
```bash
ansible [core 2.14.18]
  config file = None
  configured module search path = ['/home/debian/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  ansible collection location = /home/debian/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/bin/ansible
  python version = 3.11.2 (main, Nov 30 2024, 21:22:50) [GCC 12.2.0] (/usr/bin/python3)
  jinja version = 3.1.2
  libyaml = True
```
### Ansible playbook
1. Create hello_ansible.yaml file.
2. Run file:
```ansible-playbook hello_ansible.yaml```
