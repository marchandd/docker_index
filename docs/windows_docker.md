# Be Docker ready on Microsoft Windows for GUI Virtual Environment Studies

## Goal

Install all software to display GUI Virtual Environment Studies Docker images on Microsoft Windows.

### Prerequisites

- 64-bit Windows guest OS.
- Processor that needs to support hardware virtualization.
- Have at least 4 Gb RAM with 2Gb reserved to Docker VM.

### Downloads

[Docker](https://github.com/boot2docker/windows-installer/releases "Docker")

[GUI VNC client](http://www.realvnc.com/products/vnc/ "VNC")

[GUI SSH client](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html "SSH")


## Docker

### Docker install

- Launch docker-install.exe (with right click to run as an administrator).
- Install by default on C:\Program Files\Boot2Docker for Windows.  
- Choose Full install (Boot2Docker + VirtualBox + MSYS-git UNIX tools).  
Don't forget to check "Add Boot2Docker.exe to path".  
- When asked, accept to install Oracle Corporation bus controller driver.  
- When asked, accept to install Oracle Corporation network driver 1.  
- When asked, accept to install Oracle Corporation network service.  
- When asked, accept to install Oracle Corporation network driver 2.  
- Restart computer

[For more details](http://docs.docker.com/installation/windows/ "Installation")

### Docker initiate

- On desktop click on "Boot2Docker Start" shortcut.  
- When asked, accept to install Oracle Corporation VirtualBox interface 1.  
- When asked, accept to install Oracle Corporation VirtualBox interface 2.  
You could wait some long minutes until you see screen like this:  
starting... Waiting...  
...............................ooo  
ooooooooooooooooooooooooooo  
Started.  
- Everything turned OK when you see whale logo with Boot2Docker version.

### Docker initiate trouble

It's happen when Boot2Docker window is shutting down without warning. That's mean Docker failed to initiate, so try to do:  
- Open Oracle VM VirtualBox.  
- Click on Boot2Docker-vm settings.  
- Verify you don't have "Invalid parameter detected" at the bottom of the  window...  
- Sometimes you need to raise Display/Video memory.  
- Sometimes you need to reduce System/Motherboard to have RAM < 50%.

### Docker RAM optimization

On shell CMD command, for example, raise default double memory for Docker VM like this:  
:computer: `boot2docker stop`  
:computer: `VBoxManage modifyvm boot2docker-vm --memory 4000`  
:computer: `boot2docker start`  

## GUI VNC client install

- Launch vnc_5-2-1.exe (with right click to run as an administrator).  
- Just check VNC Viewer and not VNC server (Mirror and Printer).  
- Install by default on C:\Program Files\RealVNC\VNC Viewer for Windows.  

## GUI SSH client install

- Launch putty-0.64-installer.exe (with right click to run as an administrator).  
- Install by default on C:\Program Files (x86)\PuTTY.  
- Keep association between .PPK files.
