# Setting up a new VM in Google Compute Engine

## Create VM

Create a VM via the [Google cloud console](https://console.cloud.google.com).

## Open 8080 port in the Firewall

Create a Firewall rule via the [Google cloud console](https://console.cloud.google.com).

## Setup basic packages

Access the VM via ssh and execute the following commands:

```bash
sudo apt-get update
sudo apt-get -y upgrade
sudo apt-get -y install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common \
    apache2-utils \
    git
```

## Install docker

```bash
# Get the GPG key from docker and add their repository to apt
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

# Update apt and install docker
sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose

# Add user to docker group to use docker without sudo
sudo groupadd docker
sudo gpasswd -a $USER docker

# Login to your current user to enable docker command without sudo
sudo su $USER
```
