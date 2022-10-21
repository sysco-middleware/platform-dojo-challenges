# Install and Run Tomcat9 web server 

## 1. Github

### 1.1 Install the git and configure it.

1. Install git : `sudo apt-get install git-all`
2. Configuration :  
   a. `git config --global user.email "vissi1908@gmail.com"`  
   b. `git config --global user.name "vishal-1908"`

### 1.2 ssh-keygen setup for Git

1. To generate public private key pair in Killercoda: `ssh-keygen`
2. Copy the details from id_rsa.pub(present inside .ssh folder) to the github SSH and GPG keys.

### 1.3 Git Checkout and working on feature branch

1. `git clone git@github.com:sysco-middleware/platform-dojo-challenges.git`
2. `cd platform-dojo-challenges`
3. `git checkout feature-challenge-03`
4. `git branch` - To verify the branch I'm working on. It should point to feature-challenge-03

## 2. Ansible Setup

`sudo apt install ansible`

## 3. Ansible Tasks

1. Ubuntu catalogue update  
   `ansible-playbook CatalogUpdate.yml -vvv`
2. Installation and configuration of Tomcat 9 web server  
    `ansible-playbook TomcatWebServer.yml`
3. Verify if tomcat is up and running  
    `sudo systemctl status tomcat`
  




