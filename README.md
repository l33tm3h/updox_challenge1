# UpDox Challenge 1
Write an Ansible playbook that installs Filebeat,
ElasticSearch & Kibana. Filebeat should be configured
to index /var/log/syslog (or /var/log/messages). Include
firewall rules, the ports exposed should be configurable 
with variables in Ansible. Polish it and treat it like 
it would be used in a production environment.

## Setup
 * Environment: Ubuntu 16.04 build
 * Install ansible: http://docs.ansible.com/ansible/latest/intro_installation.html
 * Setup openSSH server
 * Don't forget to add authorized_keys: http://docs.ansible.com/ansible/latest/intro_getting_started.html
 * Follow instructions: https://serversforhackers.com/c/an-ansible-tutorial
 * Assume sudo already granted to user

## Updates
Our Ansible client is going to be the same as our Ansible server.  You'll need to update /etc/ansible/hosts with the following:
  [myAnsibleServer]
  127.0.0.1

## Usage
  # if password exists on user, --ask-become-pass will be necessary
  ansible-playbook playbooks/challenge1.yml --ask-become-pass