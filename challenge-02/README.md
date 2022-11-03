Ansible playbook to Install and Run Nginx web server
1. Prerequisites
1.1 Install and Initialize git
sudo apt-get install git-all
git init

1.2 Install Ansible
sudo apt install ansible

2. Github Tasks

2.2 configure git with user credentials
git config --global user.email "<enter email associated to git user account>"
git config --global user.name "<enter git username>"

2.3 ssh-keygen generation
a. Execute the below command
ssh-keygen -t rsa -C "xyz.dummy@xyz.com"
b. Enter the file name if you want to store the ssh key in a specific file. Else it will be stored in default file. File is generated/available under folder .ssh at the location where the git repository was initiated.

2.4 ssh key addition to git profile
a. Execute the below commands
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/<enter the filename which stores the Keygen pair>
b. Copy the details from <ssh key file name as per 2.3.b>/id_rsa.pub to github SSH and GPG keys section under settings. 

2.5 Cloning of repository from github
git clone -b feature-challenge02 git@github.com:sysco-middleware/platform-dojo-challenges.git
cd platform-dojo-challenges
git branch --To validate if the current branch is pointing to feature-challenge02

2.6 
git checkout feature-challenge02
cd challenge-02
cat README.md

3. Ansible Tasks

3.1 Ubuntu catalogue update
ansible-playbook APTCatalogUpdate.yml

3.2 Nginx webserver installation
ansible-playbook NginxWebServer_Install.yml

3.3 Validate if the server is installed as expected and is up and running by executing the below command and validating the output as shown below
sudo systemctl status nginx
ubuntu $ ansible-playbook APTCatalogUpdate.yml
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [Ubuntu catalog update] *********************************************************************************************************************************************************

TASK [Gathering Facts] ***************************************************************************************************************************************************************
ok: [localhost]

TASK [Update and upgrade apt packages] ***********************************************************************************************************************************************


changed: [localhost]

PLAY RECAP ***************************************************************************************************************************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

