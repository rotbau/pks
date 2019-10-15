**GIT Commands**

Initial Configuration
** ``git config --global user.name 'My_Name'``
** ``git config --global user.email 'myEmail@wherever.com'``
** ``git config --global color.ui 'auto'``

Clone GIT Repository to Local
``git clone https://foo.bar/repository.git``
    To get specific branch
    ``git clone --branch <tag> <repo>``

Create Local Repository and Push to GIT
** create empty directory
** ``git init``
** ``git add README.MD``
** ``git commit -m "initial commit"``
** ``git remote add origin https://github.com/user/repository.git``
** ``git push -u origin master``

Push local changes to GIT repository
** Workflow: edit -> stage -> commit -> push
** ``git add .`` (commits all changes in working directory to staging area)
** ``git add hello.py`` (commits single file to staging area)
** ``git commit``
** ``git push`` 
** ``git status``



VRA4sTQRWupQwOqlJ8oI0SOCot4oVu0Wz4Rkc8IHH7Kz3yDuCEA3tyk7nNPGEEzw

curl -X POST https://console-stg.cloud.vmware.com/csp/gateway/am/api/auth/api-tokens/authorize?refresh_token=VRA4sTQRWupQwOqlJ8oI0SOCot4oVu0Wz4Rkc8IHH7Kz3yDuCEA3tyk7nNPGEEzw | jq -r '.access_token'