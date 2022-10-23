# Challenge  Platform-dojo-04
 
## Task 1
Clone the following repo: sysco-middleware/platform-dojo-challenges<br>
Create your feature branch and push it to the remote origin<br>
Start coding within the "challenge-04" folder<br>
Commit and push a small change to the README file within this folder<br>

## Task 2
Implement an Ansible Playbook which automatically installs and runs: Jetty9 web server

Considerations <br>
Ubuntu's apt-get catalog must be updated as the first (separate) task of the playbook<br>
When executing this step, an error might show up due to a broken link in the catalog; you don't need to fix this, but you will need to ignore the error and continue for your playbook to run successfully (the catalog will be updated in spite of the error)<br>
The playbook must make sure that the correct package is installed and the service up & running<br>
### Acceptance Criteria<br>
Your playbook executes properly within Katacoda and you're able to see the Jetty9 landing page in the upper frame<br>
Your pull request has been reviewed and merged by a code owner


####################################################################################################


## 1. ssh-keygen setup for Git

ssh-keygen -t ed25519 -C "ganesh.gurudu@gmail.com"<br>
eval "$(ssh-agent -s)"<br>
ssh-add ~/.ssh/id_ed25519<br>


## 2. git clone 

git clone -b feature-challenge-04 git@github.com:sysco-middleware/platform-dojo-challenges.git<br>
cd platform-dojo-challenges<br>
git status<br>
#git checkout develop <br>
git branch<br>

## 3. checkout feature branch 

git checkout  feature-challenge-04<br>
git status<br>
git branch<br>
cd challenge-04<br>


## 4. edit README.md fine 

vi README.md<br>
git status<br>


## 5.add file 

git add .<br>


## 6. configure git with credentials 

git config --global user.email "ganesh.	@gmail.com"<br>
git config --global user.name "GaneshGurudu"<br>


## 7. commit and push changes <br>

git commit -m "Ganesh challenge-04 "<br>
git push origin feature-challenge-04<br>


## 8. Add localhost to inventory 

sudo vi /etc/ansible/hosts -- for adding host details<br> 


## 9. Ansible Tasks 

Ubuntu catalogue update<br>
ansible-playbook CatalogUpdate.yml <br>
**ubuntu $ ansible-playbook Jetty9webserver.yml**<br>
\[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [Install and configuare Jetty9 web server] *******************************************************************************************************************************************

TASK [Gathering Facts] ********************************************************************************************************************************************************************
ok: [localhost]

TASK [apt-get updating repositories update_cache] *****************************************************************************************************************************************
changed: [localhost]

TASK [Install Jetty9] *********************************************************************************************************************************************************************
ok: [localhost]

TASK [start Jetty9 service] ***************************************************************************************************************************************************************
ok: [localhost]

TASK [Check url response of tomcat on server1] ********************************************************************************************************************************************
ok: [localhost]

TASK [Check url response of tomcat on server2] ********************************************************************************************************************************************
ok: [localhost]

PLAY RECAP ********************************************************************************************************************************************************************************
localhost                  : ok=6    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
