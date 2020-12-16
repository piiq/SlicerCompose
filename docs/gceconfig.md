# Setting up a new VM in Google Compute Engine

## Create VM

Create a VM via the [Google cloud console](https://console.cloud.google.com).

## Open 8080 port in the Firewall

Create a Firewall rule via the [Google cloud console](https://console.cloud.google.com).

## Setup basic packages

Access the VM via ssh

## Setup basic packages

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
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```