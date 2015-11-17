# Test environments

Return to [index](https://github.com/marchandd/docker_index "Index")

## VNC from Linux

### Linux Host builder

- KUbuntu (15.10)
- Docker (1.9.0)

### Remote GUI VNC client Linux

- KUbuntu (14.10)
- KRDC-VNC (4.14.1)  
  Adress vnc://localhost:PORT

## VNC from Windows

### Windows Host builder

- Windows (7 & 8.1)
- Docker Toolbox (1.9.0)
- VirtualBox (5.0.9)
- MsysGit (2.6.3)

### Remote GUI VNC client Windows

- Windows (7 & 8.1)
- Vnc-viewer (5.2.1)  
  Address Boot2Docker_IPv4:PORT

Remark:  
Docker is accessing on Windows only through VirtualBox network interface. 
So, using 127.0.0.1 is not possible...
- You must choose Docker_IPv4 remained at boot start into the 
dedicated console.
First time you logged with Vnc-viewer:  
- You can have unsecured channel warning message because SSL is not activated.

## SSH from Linux

### Linux Host builder

- KUbuntu (15.10)
- Docker (1.9.0)

### Remote Terminal SSH client Linux

- KUbuntu (15.10)
- ssh  
  Address -X root@IPv4 -p PORT

## SSH from Windows

### Windows Host builder

- Windows (7 & 8.1)
- Docker Toolbox (1.9.0)
- VirtualBox (5.0.9)
- MsysGit (2.6.3)

### Remote GUI SSH client Windows

:warning: Make sure X11 forwarding is enabled into SSH/X11 Configuration.

- Windows (7 & 8.1)
- Docker Toolbox (1.9.0)
- VirtualBox (5.0.9)
- MsysGit (2.6.3)
- PuTTY (0.64)  
  Address Docker_IPv4:PORT

Remark:  
Docker is accessing on Windows only through VirtualBox network interface. 
So, using 127.0.0.1 is not possible...  
- You must choose Docker_IPv4 remained at boot start into the dedicated console.

## Docker containers

### Classic container

- Ubuntu (14.10)

### Wine container

Acces with Root account:
- Ubuntu (14.10)
- Wine (1.17.50)
- Winetricks with options:  
  win7
  mfc42
  windowmanagermanaged=n
  sandbox
