1,https://github.com/
Sign up for GitHub (email and password)
Sign in with linquanhao@126.com	 mo****2o

Create a New Repository  https://github.com/linquanhao/MyGitHub
Public: free
Private: fee

2,Install msysgit 
Git-1.8.3-preview20130601.exe, this is command line utils
TortoiseGit : GUI based on msysgit

Start->All Programs->Git->Git GUI
Create New Repository with local folder, for example C:\Training\GitHub\LocalRepo
git init

after create, there is .git file under that folder

after install msysgit, there are right click menu item, 'Git Bash Here' 'and Gti GUI Here'

3, create ssh key
under local folder, right click 'Git Bash Here'

ssh-keygen -t rsa -C "linquanhao@126.com"
follow the steps and input password, there will be a .ssh folder generated under ~/ (home dir), in my env it is  n:\.ssh
open (home fir):\.ssh\id_rsa.pub, copy the key
return to github, go to Account Settings->SSH Keys->Add SSH key->Input Title->Copy rsa key, Click 'Add key

4, test connect github server
ssh -T git@github.com

problem here:
ssh:github.com: no address associated with name
resolve: SAP-Internet, you may re-do step3 to create ssh key


5, upload local repo to github
record your name and email
git config --global user.name "linquanhao"
git config --global user.email "linquanhao@126.com"

git remote add origin git@github.com:linquanhao/MyGitHub

//add file into local repo
git add readme.txt
git commit -m "first commit"
//pull first from github
git pull origin master
//upload to github
git push origin master


