# Install and Run Lightptd web server

## 1. Ansible Setup

sudo apt install ansible

## 2. Ansible Tasks

1. Catalog update

	ansible-playbook catalogUpdate.yml

2. Install & run Lightptd

	ansible-playbook lightptd.yml
