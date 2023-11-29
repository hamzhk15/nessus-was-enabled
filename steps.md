# Here is the steps you need to follow to download and install Ubuntu VM with Nessus and WAS module enabled

#### Download Ubuntu 22.04.3 LTS from here: https://ubuntu.com/download/desktop

#### Install Ubuntu Desktop on new virtual machine – step by step guide can be found here: https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview

#### Install curl tool: 
```sudo snap install curl

#### Download Nessus by run the following command: 
```curl --request GET  --url 'https://www.tenable.com/downloads/api/v2/pages/nessus/files/Nessus-10.6.3-debian10_amd64.deb' --output 'Nessus-10.6.3-debian10_amd64.deb'

#### Install Nessus by run the following command: 
```sudo dpkg -i Nessus-10.6.3-debian10_amd64.deb

#### Install Docker as follows: 

#### Add Docker's official GPG key: 
```sudo apt-get update sudo apt-get install ca-certificates curl gnupg 
sudo install -m 0755 -d /etc/apt/keyrings curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg 
sudo chmod a+r /etc/apt/keyrings/docker.gpg
``` 

#### Add the repository to Apt sources: 
```echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null 
sudo apt-get update
``` 

#### Install docker 
```sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
