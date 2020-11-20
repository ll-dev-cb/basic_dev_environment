# basic_nodejs_express
Instructions for seting up local server on any machine

asumption is you need a virtual machine first
if you dont have any handy, do this:

1. download virtualbox for your operating system
https://www.virtualbox.org/wiki/Downloads

2. download ubuntu (Desktop is easier, but server uses less resources)
Desktop - https://ubuntu.com/download/desktop
Server -  https://releases.ubuntu.com/20.04/ubuntu-20.04.1-live-server-amd64.iso

Create new VM in Virtualbox
if asked for .iso point to downloaded ubuntu image 

defaults are ok - can be changed later as CPUs or memory
Networking can either be shared or bridged - however the IP number needs to be known for remote login

-after install create snapshot to save initial state of VM

once ubuntu vm runs open terminal and type

sudo apt install openssh-server

this will allow remote login to the VM

ifconfig 
or
ip link

will list all network interfaces eg "eth0 192.168.2.10"

the ip is used for ssh

from host machine logon to VM with

ssh username@192.168.2.10
answer yes
and type password

now to install node type:

sudo apt install nodejs

after this the command "npm" is available, this will further allow to install node modules.


# install projects
typically one would use "git clone URL" to install an existing project

simple demo:

git clone https://github.com/do-community/ejs-demo

tutorial:
https://www.digitalocean.com/community/tutorials/how-to-use-ejs-to-template-your-node-application



advanced demo with Database
clone this repository:
git clone https://github.com/WebDevSimplified/Markdown-Blog

needs database installed
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/










