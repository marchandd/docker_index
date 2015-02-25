# Test environments

Return to [index](https://github.com/marchandd/docker_index "Index")

## VNC from Linux

### Linux Host builder

- KUbuntu (14.10)
- Docker (1.4.1)

### Remote GUI VNC client Linux

- KUbuntu (14.10)
- KRDC-VNC (4.14.1)  
  Adress vnc://localhost:PORT

## VNC from Windows

### Windows Host builder

- Windows (7 & 8.1)
- Boot2Docker (1.4.1)
- VirtualBox (4.3.20)
- MsysGit (1.9.4)

### Remote GUI VNC client Windows

- Windows (7 & 8.1)
- Vnc-viewer (5.2.1)  
  Address Boot2Docker_IPv4:PORT

Remark:  
Docker is accessing on Windows only through VirtualBox network interface. 
So, using 127.0.0.1 is not possible...
- You must choose Boot2Docker_IPv4 remained at boot start into the 
dedicated console.

## SSH from Linux

### Linux Host builder

- KUbuntu (14.10)
- Docker (1.4.1)

### Remote Terminal SSH client Linux

- KUbuntu (14.10)
- ssh  
  Address -X root@IPv4 -p PORT

## SSH from Windows

### Windows Host builder

- Windows (7 & 8.1)
- Boot2Docker (1.4.1)
- VirtualBox (4.3.20)
- MsysGit (1.9.4)

### Remote GUI SSH client Windows

:warning: Make sure X11 forwarding is enabled into SSH/X11 Configuration.

- Windows (7 & 8.1)
- Boot2Docker (1.4.1)
- VirtualBox (4.3.20)
- MsysGit (1.9.4)
- PuTTY (0.64)  
  Address Boot2Docker_IPv4:PORT

Remark:  
Docker is accessing on Windows only through VirtualBox network interface. 
So, using 127.0.0.1 is not possible...  
- You must choose Boot2Docker_IPv4 remained at boot start into the dedicated console.

## Docker containers

### Classic container

- Ubuntu (14.10)

### Wine container

Acces with Root account:
- Ubuntu (14.10)
- Wine (1.17.33)
- Winetricks with options:  
  win7
  mfc42
  windowmanagermanaged=n
  sandbox
