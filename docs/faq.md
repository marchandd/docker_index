# Frequently asked questions

Return to [index](https://github.com/marchandd/docker_index "Index")

## Problem to access to Docker with non root account

If you have this message:  
FATA[0000] Get http:///var/run/docker.sock/v1.17/images/json: dial unix /var/run/docker.sock: permission denied. Are you trying to connect to a TLS-enabled daemon without TLS?

Proceed like this with current account:  
- :computer: `ls -l /var/run/docker.sock` to confirm problem.
- :computer: `sudo gpasswd -a ${USER} docker`
- :computer: `cat /etc/group | grep ^docker` if confirmed.
- :computer: `groups` to be sure.
- :computer: `sudo service docker restart`

If always none access, restart your machine.  
[More details here](http://dev-maziarz.blogspot.fr/2015/01/running-docker-sock-permission-denied.html "Information")

## Direct access

Enter directly into container with [Nsenter](http://mozdef.readthedocs.org/en/latest/installation.html "Nsenter")

## VNC access

### In case of crash

Sometimes happen when mouse is not available and you can't interact with container X display.

Proceed like this:  
- Disconnect container from VNC.
- :computer: Open console with `sudo su`.
- :computer: Run `docker ps -a`  
  Search container name.  
  Identify ContainerID.
- :computer: Run `docker stop ContainerID`.
- :computer: Run `docker start ContainerID`.
- Connect container from VNC.

## SSH access

### In case of crash

Sometimes happen when GUI apps is sleeping and you can't interact with container X display.

Proceed like this:  
- Stop and disconnect container from SSH terminal:  
:computer: Enter `ctrl+c`  
:computer: Enter `exit`  
- If you are not return to your current prompt:
:computer: Enter `ctrl+c`  

- :computer: Open console with `sudo su`.
- :computer: Run `docker ps -a`  
  Search container name.  
  Identify ContainerID.
- :computer: Run `docker stop ContainerID`.
- :computer: Run `docker start ContainerID`.
- Connect container from SSH terminal.
