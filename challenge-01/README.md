# Install Apache Server 

## 1. Catalog.yml Playbook
apt-get is a command line tool for interacting with the Advanced Package Tool (APT) library.
It allows you to search for, install, manage, update, and remove software.

## 2. Apache2WebServer.yml Playbook

#### 2.1 Install Apache2 WebServer
This playbook will install Apache Webserver

#### 2.2 Update the Firewall 
Update the policy to allow Apache using UFW

#### 2.3 Check if the Apache Server is started

## 3. To run the playbook, we have to use below commands:
ansible-playbook Apache2WebServer.yml --ask-become-pass -vvv

