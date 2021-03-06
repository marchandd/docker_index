# Be Docker ready on Linux Ubuntu for GUI Virtual Environment Studies

Return to [index](https://github.com/marchandd/docker_index "Index")

## Goal

Install all software to display GUI Virtual Environment Studies Docker images on Linux Ubuntu 14.04/15.10.

:warning: All shell command are run under root account.

### Prerequisites

- 64-bit Linux Ubuntu guest OS.
- Processor that needs to support hardware virtualization.
- Have at least 4 Gb RAM with 2Gb reserved to Docker VM.

## Docker:copyright:

### Downloads (> v1.7)

:computer: `sudo su`  
:computer: `sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D`  
For Ubuntu 14.04 only:  
:computer: `sh -c "echo deb https://apt.dockerproject.org/repo ubuntu-trusty main\> /etc/apt/sources.list.d/docker.list"`  
For Ubuntu 15.10 only:  
:computer: `sh -c "echo deb https://apt.dockerproject.org/repo ubuntu-wily main\> /etc/apt/sources.list.d/docker.list"`  
:computer: `sudo apt-get update`  
Delete older version with:  
:computer: `sudo apt-get purge lxc-docker`  
Update with:  
:computer: `sudo apt-get update`  
And now you can prepare install:  
:computer: `sudo apt-get install linux-image-extra-$(uname -r)`  

### Docker install

:computer: `sudo apt-get install docker-engine`  

[For more details](https://docs.docker.com/installation/ubuntulinux/ "Installation")

### Docker verification

Display the version with command:  
:computer: `docker -v`  

## GUI VNC:copyright: client install

Main software are already installed with Ubuntu distributions but you can access to it with:  
- On Gnome : Menu > Internet >  Terminal Server Client:copyright:
- On KDE : Kmenu > Internet > KRDC-VNC:copyright:

[For more details](https://help.ubuntu.com/community/VNC/Clients/ "VNC")

## OpenSSH:copyright: client

### OpenSSH client install

Already installed with Ubuntu distributions but you can test it with:  
:computer: `ssh -V`  
:computer: `dpkg -l libssl*`  
Otherwise install it with command:  
:computer: `sudo apt-get install openssh-client`  

### Key generation

To make key creation with PassPhrase enter:  
:computer: `ssh-keygen -t rsa`  
Private key could be seen with:  
:computer: `cat /root/.ssh/id_rsa`  
Public key could be seen with:  
:computer: `cat /root/.ssh/id_rsa.pub`  

[For more details](https://help.ubuntu.com/community/SSH/ "SSH")
