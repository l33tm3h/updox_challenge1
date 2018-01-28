# UpDox Challenge 1
Write an Ansible playbook that installs Filebeat,
ElasticSearch & Kibana. Filebeat should be configured
to index /var/log/syslog (or /var/log/messages). Include
firewall rules, the ports exposed should be configurable 
with variables in Ansible. Polish it and treat it like 
it would be used in a production environment.

## Setup
### OS
 * Environment: Ubuntu 16.04 build
 * Setup openSSH server
 * Don't forget to add authorized_keys: <http://docs.ansible.com/ansible/latest/intro_getting_started.html>
 * Setup sudo for user you will connect as: <http://mixeduperic.com/ubuntu/how-to-setup-a-user-or-group-with-sudo-privileges-on-ubuntu.html>

### Ansible
 * Install ansible: <http://docs.ansible.com/ansible/latest/intro_installation.html>
 * Follow instructions: <https://serversforhackers.com/c/an-ansible-tutorial>

Our Ansible client is going to be the same as our Ansible server.  You'll need to update /etc/ansible/hosts with the following:
  [local]
  127.0.0.1

Updating Filebeat

Updating firewall settings

### Running Ansible
To validate your playbook is formatted correctly, use the `-C` flag:
  `ansible-playbook -vvvv -C playbooks/install_software.yml --ask-become-pass`

To setup the software using Ansible:
  `ansible-playbook -vvvv playbooks/install_software.yml --ask-become-pass`

To initiate the services we just installed:
  `ansible-playbook -vvvv playbooks/start_services.yml --ask-become-pass`
