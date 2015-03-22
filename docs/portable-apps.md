Complete image ready dedicated Windows portable-apps emulate compatibles
========================================================================

Return to [index](https://github.com/marchandd/docker_index "Index")

Goal
----

Use Docker container to install easily Windows apps on Linux environment.  
Container permits to test apps into independent environment from the host 
without have to install locally Wine emulator and VNC or SSH servers.  
Dedicated to user non-computer specialist, scripts and commands are reduced to minimum.  
VNC client: SSL usage is not available for have less software to install.  
SSL client: user & password usage is only available (not secret-key value).

Only 10 minutes to have 5 Portable-Apps ready to run with only 10 scripts to 
launch without parameter and just 1 command line to run !

Take precaution when you use it because portability is not guaranteed...  
Software samples proposed are available with 50 to 100 % functional features 
but it's sufficient to discover great software !  
I recommend to use these great software in last version on Windows OS,
but take advantage to discover them in isolated Linux environment into 
Docker containers.

Softwares tested
----------------

| State | Portable-app  
| --- | ---  
| Silver | ToDoList ZIP-app  
| Silver | FreeCommander Portable-app  
| Gold | Notepad++ Portable-app  
| Gold | WinMerge Portable-app  
| Gold | AntRenamer Portable-app  
| Gold | 7-Zip Portable-app  

Dockerfile explanation
----------------------

### Softwares ready to install after download

Graphical user interface portable software presents are:
- ToDoList by AbstractSpoon to manage Todo lists with tree-view and 
calendar display.
- FreeCommander (old version) by Marek Jasinski to manage files and directories 
with multi-tools.
- Notepad++ by Notepad++Team to edit source code supporting several languages.
- WinMerge by Dean P. Grimm / Thingamahoochie software to differencing and 
merge files and directories.
- AntRenamer by Antp.be to rename files and directories.
- 7-Zip by 7-Zip developers to archive and extract supported a lot of formats with a powerfull File manager.

### Work-flow: 10 minutes to have 5 Portable-Apps ready to run !

- Download software from file with all URLs inside.
- Search last version for Portable-App to download (Dedicated samples Windows only).
- Copy files scripts to install software in container into /root/Downloads 
  directory.
- Give permission to run EXE and SH files.
- Set up directory access.

Session explanation
-----------------------

### 1 minute to set Wine emulator !

First, scripting Wine through Winetricks software options.

Script behaviours:
- Prepare Wine user directory.
- Sandbox mode to limit actions for Windows software set.
- Windows 7 environment set.
- Disallow the window manager to decorate the windows.
- Install mfc42 usage for Visual C++ 6 apps.
- If '/data/' directory is presents into container, a symbolic link is created with "C:\users\Public\Documents" available on Windows Portable-apps.

### Few seconds for each Zip-apps install !

Scripting Zip-apps install and alias ready. Use default values to install.

Script behaviours:
- Remove older installed version software.
- Unzip new version software and give permission to run it into target directory.
- Remove older installed version alias.
- Make new version software alias.
- Install and running logs are save into files.
- Remarks: running alias launched software install.

### Few seconds for each Portable-apps install !

Scripting in two steps Portable-apps (EXE) install and to be alias ready.
Use default values to install.

Scripts behaviours:
- Remove older installed version software.
- Copy from /root/Downloads/ to a Wine installer directory.
- Run new version installer and give permission to run it into target directory.
- Remove older installed version alias.
- Make new version software alias.
- Install and running logs are save into files.

### Into Dedicated samples Windows Portable-app, only 1 script from install to launch !

- Run one same aliasname.sh command in cyclic mode to run sub programs:  
One run to set Wine emulator, one run to install and one run to launch.  
- Alias is not available at the end of program. You have to make alias activation later.

### Don't remember alias activation !

:warning: Alias have not automatic recognition:
- Run `source ~/.bashrc` command to enable alias access from command line.

### 1 minute when upgrading Portable-Apps versions !

- Make sure new version have same install Features that older and after: 
- Change URLs in /root/Downloads/downloadsLinks.txt file.
- Delete /root/Downloads/old versions XX Portable-Apps
- Run /usr/local/sbin/install_XXPortable.sh
- Run /usr/local/sbin/postInstall_AliasForXXPortable.sh (if EXE program).
- Run `source ~/.bashrc` command to update alias.  
That all to do !
