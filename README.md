# Ansible Playbook 

Tested on Ubuntu 15.04 64bit and OSX Yosemite


Contains the following roles:
* caddy-ssl-proxy - Installs caddy as an ssl proxy (Ubuntu)
* docker - Docker from the official Docker repo       
* fail2ban - Installs fail2ban (Ubuntu)       
* gcloud - Installs the google cloud sdk + utils (Ubuntu)        
* madsonic-docker - Launches Madsonic docker container as a systedmd service (Ubuntu)
* nginx-ssl-proxy - Installs nginx as an ssl proxy (Ubuntu) 
* plex-docker -  Launches Plex docker container as a systedmd service (Ubuntu)    
* sshd - Custom sshd (Ubuntu)            
* vim - Vim with vundle, vim-go and others take a look at the role
* deluge-docker - Launches Deluge docker container as a systedmd service (Ubuntu)   (Ubuntu)
* firewall - Configures IPtables (Ubuntu)   
* golang - Latest Go build tools (Ubuntu)          
* nethogs - Builds installs nethogs ip traffic monitoring tool (Ubuntu) 
* ohmyzsh - Installs Oh-My-ZSH (Ubuntu & OSX)
* powerline_fonts - Fonts for Oh-My-Zsh agnoster theme (Ubuntu & OSX)
* terminator - Installs Term GUI (Ubuntu)
* pxe-boot - (Centos 7 only) PXE server with DHCP Proxy, tftp, http file server to boot Coreos. Used with Vmware Fusion


Please edit the laptop.yml or mac.yml to change user and user group variables. 

## Agnoster Theme
You will need to set your preferred terminal to use one of the powerline fonts in order for the agnoster prompt to be displayed easily. I recommend Hack or Deja Vu Sans Powerline. 

## Oh-My-Zsh and Enviromental Vars

* Edit the roles/ohmyzsh/vars/main.yml to export any enviromental variables you might have. 
* You can also change the default theme and oh-my-zsh plugins here.  

# Ubuntu
```
git clone https://github.com/dbnegative/ansible.git ~/ansible
cd ~/ansible
ansible-playbook laptop.yml -K
```
# OSX  
Please install Xcode with commandline tools and ansible though homebrew first.
```
brew install ansible
git clone https://github.com/dbnegative/ansible.git ~/ansible
cd ~/ansible
ansible-playbook mac.yml -K
```

