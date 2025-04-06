# Devops-DemoAnsible
This is a demo repository for Gilde opleidingen to share and show some Ansible playbooks and instructions

## Clone the repository
install git on the ansible machine<br/> 
clone the repo Devops-Demo Ansible
```
git clone https://github.com/MG-Polo/Devops-DemoAnsible
```

## Get the right files
switch to the right branch for the playbooks
```
git checkout Playbooks
```

Copy the host file from the git to the Ansible directory<br/> 
On your Ansible VM try to SSH to the following VM's:
  - Ubuntu server 1
  - Ubuntu server 2
  - Router PFSense
If SSH to PFSense doesn't work maybe this link can help you<br/> 
https://docs.netgate.com/pfsense/en/latest/recipes/ssh-access.html

## Ping with Ansible
try to ping all of the hosts with ansible<br/> 
```
ansible -i hosts all -m ping
```

#Why doesn't it work? 
Are your hosts the same as my hosts?<br/> 
Make sure you have your PFSense data and your Ubuntu server data in the hosts file.<br/> 
These VM's need to be in the file:
  - Ubuntu server 1
  - Ubuntu server 2
  - Router PFSense

try again to ping all of your hosts<br/> 

## Run the intro playbook
Now try to run the playbooks and look what happens
```
ansible-playbook intro_playbook.yml
```
# create users
Now on the ubuntu servers you need to create the users John, Allex and Megan.<br/> 
Do this in one playbook.

## Copy files to the servers
Next we need to copy some file to the servers.<br/> 
You can do this with the playbook CopyFile.yml<br/> 
The file is named dino.pic, this file needs to be in the file directory as specified in the playbook.<br/> 
After you run the playbook, connect to both servers and verify that the image is there.<br/> 

## PFSensible
For the next step we need to instal pfsensible on our Ansible host.<br/> 
Do this with the following command
```
ansible-galaxy collection install pfsensible.core
```

## PFSense playbook
For the next steps we need to do some portforwarding on the PFSense.<br/>
We need to do this for port 80 and 443.<br/> 
Look at the PFSense playbook and edit it to do portforwarding for port 80 and 443

## Webserver
Now we can create a webserver.<br/>
In the hosts file create a group for the webserver. <br/>
This can be Ubuntu server 1 or 2. Make a wise choice ;).<br/>

If you edited the hosts file, you can inspect the webserver playbook.<br/>
Change what you need to change to make it work.<br/>


