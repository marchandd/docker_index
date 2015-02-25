# Frequently asked questions

Return to [index](https://github.com/marchandd/docker_index "Index")

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
