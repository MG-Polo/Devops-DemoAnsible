# Devops-DemoAnsible
This is a demo repository for Gilde opleidingen to share and show some Ansible playbooks and instructions

install git on the ansible machine
clone the repo Devops-Demo Ansible
git clone https://github.com/MG-Polo/Devops-DemoAnsible

switch to the right branch for the playbooks
git checkout Playbooks

Copy the host file from the git to the Ansible directory
On your Ansible VM try to SSH to the following VM's:
  - Ubuntu server 1
  - Ubuntu server 2
  - Router PFSense
If SSH to PFSense doesn't work maybe this link can help you
https://docs.netgate.com/pfsense/en/latest/recipes/ssh-access.html

try to ping all of the hosts with ansible
ansible -i hosts all -m ping

Why doesn't it work? are your hosts the same as my hosts?
Make sure you have your PFSense data and your Ubuntu server data in the hosts file.
These VM's need to be in the file:
  - Ubuntu server 1
  - Ubuntu server 2
  - Router PFSense

try again to ping all of your hosts

Now try to run the playbooks and look what happens
ansible-playbook intro_playbook.yml

Now on the ubuntu servers you need to create the users John, Allex and Megan.
Do this in one playbook.

Next we need to copy some file to the servers.
You can do this with the playbook CopyFile.yml
The file is named dino.pic, this file needs to be in the file directory as specified in the playbook.
After you run the playbook, connect to both servers and verify that the image is there.

For the next step we need to instal pfsensible on our Ansible host.
Do this with the following command
```
ansible-galaxy collection install pfsensible.core
```


*Change hostname of the firewall -> create playbook
*setup webserver -> create playbook


