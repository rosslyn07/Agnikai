- first i created a private repo in my alt git hub account 
- then i came back to my terminal ( preferably a new one ) and type the following line below 
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```
- after generating the ssh key after following the default procedure run the following code below and add the ssh keys to the ssh agent 
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_youruniqueid
```
- in the config files created add the below lines of code 
```
Host github.com-anynameyouwanttogive
HostName github.com
User git
IdentityFile ~/.ssh/id_ed25519_youruniqueid
```
- after settings these things up cat into the id_ed.pub files and copy the ssh key and paste it into the git hub ssh key section 
- for testing if the ssh if setup correctly type this below code 
```
ssh -T git@github.com-namethatyougave
```
- after doing all these things go to the private repo and copy the ssh link of the repo and make changes in the ssh like below
```
git@github.com-dumpyard:dumpyard1729/AgniKai.git
```
- after the repo is cloned locally config the local settings like below making this is kinda necessary because it will commit from this account instead of the the global set config 
```
git config user.name "your_user_name"
git config user.email "your_email_id"
```
- you are good to go 

# how did i setup the same of my phone 

- first i downloaded termux app form the fdroid site 
- then i installed the below packages 
```
pkg install git openssh
pkg install gh 
```
- after installing the gh package run the below code and follow the steps 
```
gh auth login 
```
- after loging in i cloned the private repo using gh repo link from the github site 
- you are good to go 