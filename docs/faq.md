# Frequently asked questions

Return to [index](https://github.com/marchandd/docker_index "Index")


## Problems to put Docker commands with Docker Quick Start on Window after reboot

If you can't have access to Docker admin commands (docker images, docker ps -a, ...) and you have this message:  
Error running connection boilerplate: Error checking and/or regenerating the certs: There was an error validating certificates for host "192.168.99.100:2376": dial tcp 192.168.99.100:2376: connectex: No connection could be made because the target machine actively refused it.  
You can attempt to regenerate them using 'docker-machine regenerate-certs name'. Be advised that this will trigger a Docker daemon restart which will stop running containers.

It seem to be a bug from Docker Toolbox (> v1.8) and Git.  
Just double click on Kitematic icon from desktop and use CLI button to open Powershell prompt.  
All commands could now work from this window.

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

## Direct container access

Enter directly into container with [Nsenter](http://mozdef.readthedocs.org/en/latest/installation.html "Nsenter")

## VNC container access

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

## SSH container access

### Find Docker IP on Windows for SSH Client access

If you don't know which IP address to put in your SSH client, just double click on Docker Quick Start icon from desktop.  
When finished display at the end of the prompt, you will see your IP adress.  
With one Network card on Windows, IP by default is 192.168.99.100

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

## Problem inside containers

### Problems to share data between Window user and containers

If you are on Window and you want to share data with your containers during RUN process with V option, you must respect Linux path.  
It failed when you are not give correct Drive access.

Proceed like this:  
- For example to share C:\Users\ZZZZ\:
:computer: Enter `docker run -d -p 192.168.99.100:YYYYY:22 --name latest_container -v //c/Users/ZZZZZ/_temp:/data container`  

### Wine initialization messages

If you see this message:  
Executing wine /root/.cache/winetricks/vcrun6/vc6redistsetup_deu.exe /T:C:\windows\Temp\_mfc42 /c /q
err:xrandr:xrandr12_init_modes Failed to get primary CRTC info.
fixme:ole:RemUnknown_QueryInterface No interface for iid {00000019-0000-0000-c000-000000000046}
err:xrandr:xrandr12_init_modes Failed to get primary CRTC info.
Xlib:  extension "MIT-SHM" missing on display "localhost:10.0".

It seem to be a new problem with Wine or Winetricks (to easily setup Wine).  
Display is OK for me in my test environment but if you have problem to display Portable Apps on Windows, install and use XMing and MobaXTerm.

### The Portable Apps window disappears during installation or execution with SSH

This happens when multiple windows are open simultaneously.  
In fact, the window of emulated software is passed in the background (lost of focus).  
Just minimize opened windows that prevent to perceive the missing window