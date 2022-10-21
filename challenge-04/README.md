
ssh-keygen -t ed25519 -C "ganesh.gurudu@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519


git clone -b feature-challenge-04 git@github.com:sysco-middleware/platform-dojo-challenges.git
cd platform-dojo-challenges
git status
#git checkout develop 
git branch
git checkout  feature-challenge-04
git status
git branch
cd challenge-04
vi README.md
git status
git add .

git config --global user.email "ganesh.	@gmail.com"
git config --global user.name "GaneshGurudu"

git commit -m "Ganesh challenge-04 "

git push origin feature-challenge-04


sudo vi /etc/ansible/hosts -- for adding host details 


ubuntu $ ansible-playbook Jetty9webserver.yml
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
