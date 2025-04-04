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
