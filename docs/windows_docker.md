# Be Docker ready on Microsoft Windows for GUI Virtual Environment Studies

Return to [index](https://github.com/marchandd/docker_index "Index")

## Goal

Install all software to display GUI Virtual Environment Studies Docker images on Microsoft Windows.

### Prerequisites

- 64-bit Windows guest OS.
- Processor that needs to support hardware virtualization.
- Have at least 4 Gb RAM with 2Gb reserved to Docker VM.

### Downloads (> v1.7)

[Docker:copyright:](https://github.com/docker/toolbox/releases/ "Docker Toolbox")

[GUI VNC:copyright: client](http://www.realvnc.com/products/vnc/ "VNC")

[GUI PuTTY:copyright: SSH client](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html "SSH")

Optional for SSH

[GUI XMing:copyright: client](http://www.straightrunning.com/XmingNotes/ "SSH+")

[GUI MobaXterm:copyright: client](http://mobaxterm.mobatek.net/download.html "SSH+")

## Docker

### Docker install

- Launch DockerToolbox-1.9.0.exe (with right click to run as an administrator).
- Install by default on C:\Program Files\Docker Toolbox.  
- Choose Full install (Docker Client:copyright: + Docker Machine:copyright: + Kitematic:copyright: + VirtualBox:copyright: + MSYS-git:copyright: UNIX tools).  
- When asked, accept to install Oracle Corporation bus controller driver.  
- When asked, accept to install Oracle Corporation network driver 1.  
- When asked, accept to install Oracle Corporation network service.  
- When asked, accept to install Oracle Corporation network driver 2.  
- Restart computer

[For more details](http://docs.docker.com/engine/installation/windows/ "Installation")

### Docker initiate

- On desktop click on "Docker Quickstart Terminal" shortcut.  
- When asked, accept to install Oracle Corporation VirtualBox interface 1.  
- When asked, accept to install Oracle Corporation VirtualBox interface 2.  
You could wait some long minutes until you see screen like this:  
starting... Waiting...  
...............................ooo  
ooooooooooooooooooooooooooo  
Started.  
- Everything turned OK when you see whale logo with Docker version.

### Docker usage to favour

- On desktop click on "Kitematic (Alpha)" shortcut.  
If Docker VM is not started yet, Kitematic start it automatically.  
- Click on left bottom (CLI) button to open PowerShell terminal and manage Docker images.  
To manage containers, you can add new one pressing + button or manage existing ones on the list.  
This is the best easy solution to stop/start containers.

## GUI VNC client install

- Launch vnc_5-2-1.exe (with right click to run as an administrator).  
- Just check VNC Viewer and not VNC server (Mirror and Printer).  
- Install by default on C:\Program Files\RealVNC\VNC Viewer for Windows.  

## GUI SSH client install

### Main software

- Launch putty-0.64-installer.exe (with right click to run as an administrator).  
- Install by default on C:\Program Files (x86)\PuTTY.  
- Keep association between .PPK files.  
I recommended you to saved sessions for containers (without saving password).

### Optional softwares

Sometimes SSH display causes difficulties and there are software that can greatly help you.  

Xming to help export display  
- Launch Xming-6-9-0-31-setup.exe (with right click to run as an administrator).  
- Choose full installation.  
- Install by default on C:\Program Files (x86)\Xming.  

MobaXterm to help to manage SSH access  
- Extract MobaXterm_v8.2.zip to C:\Program Files (x86)\ diretory.  
- Launch MobaXterm_Personal_8.2.exe (with right click to run as an administrator).  
- Click right on Saved sessions and select Import PuTTY sessions.
