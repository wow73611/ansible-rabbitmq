About
=====

Install rabbitmq service and cluster with [Ansible](https://www.ansible.com/).

Ansible is a radically simple IT automation platform that makes your applications and systems easier to deploy.


Requirements
=====

- OS: Ubuntu 14.04 (trusty)
- [Ansible >= 2.0](https://github.com/ansible/ansible)


Usage
=====

Deploy docker with hosts file (Make sure hosts file is you need)
```
ansible-playbook -i hosts playbook.yml
```

Run as other users or use sudo
```
ansible-playbook -i hosts playbook.yml \
-e "ansible_ssh_pass=secret ansible_sudo_pass=secret sudo=yes"
```


Ansible Variables
=====

* rabbitmq_enable_cluster: Enable to create the rabbitmq cluster (Default: false)
* rabbitmq_cluster_master: Specify the master node of rabbitmq cluster (Default: Localhost)
* rabbitmq_plugins: Rabbitmq plugins to install (Default: rabbitmq_management)
* rabbitmq_remove_users: Users to remove (Default: guest)
* rabbitmq_users: Users to create (Default: admin)
