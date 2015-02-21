# Docker Containers Studies

## Aim

The goal of this approach is to provide Docker containers dedicated to facilitate Windows/Linux cross-over usage.

Studies are splitted into three domains : 
- Diversity of methods to produce GUI containers to access to Firefox.
- Mono environment to make possible to run Console or Gtk applications.
- Windows Portable-apps (global or dedicated) running with Wine emulator.
 
Experiment by yourself all approaches studies with the links below for Docker containers.

### Mozilla Firefox (Method differences for GUI containers)

Last version of Mozilla Firefox ready to use.

:checkered_flag: [X11shared (sudoers)](https://github.com/marchandd/term_x11shared_sudoers_firefox/ "X11shared") but dangerous access permissions... 

:checkered_flag: [VNC (root with xvfb & wine)](https://github.com/marchandd/vncxvfb_wine_firefox/ "VNC") with VNC protocol but not crypted... 

:checkered_flag: [SSH (root)](https://github.com/marchandd/term_ssh_root_firefox/ "SSH") 

:checkered_flag: [SSH (non root user)](https://github.com/marchandd/term_ssh_user_firefox/ "SSH") 

![Graph1](graph1.gif)

### Mono Environment

Last version of Mono environment ready to be exploited for Mono app.

:checkered_flag: [Mono Docker official (SSH root)](https://github.com/marchandd/term_ssh_root_mono/ "SSH") A Docker official version but not mono-complete. 

:checkered_flag: [Xamarin:copyright: Mono-complete install (SSH user)](https://github.com/marchandd/term_ssh_user_monodotnet45/ "SSH")

Last version of Mono environment IDE ready to use.

:soon: [Xamarin:copyright: MonoDevelop IDE (SSH user)] (https://github.com/marchandd/term_ssh_user_monodevelop/ "SSH")

![Graph2](graph2.gif)

### Multiple Windows Portable-apps

Windows Portable-apps samples easy to install, update and use.

:checkered_flag: [Windows Portable-apps samples (VNC)](https://github.com/marchandd/vncxvfb_wine_portable-apps/ "VNC") 

:soon: [Windows Portable-apps samples (SSH root)](https://github.com/marchandd/term_ssh_root_portable-apps/ "SSH")

![Graph3](graph3.gif)

### Specific Windows Portable-apps

Windows Portable-apps samples dedicated easy to install, update and use.

:checkered_flag: [Antp.be:copyright: AntRenamer Portable (SSH root)](https://github.com/marchandd/term_ssh_root_antrenamer/ "SSH") 

:checkered_flag: [Marek Jasinski:copyright: FreeCommander Portable (SSH root)](https://github.com/marchandd/term_ssh_root_freecommander/ "SSH")  

:checkered_flag: [Notepad++Team:copyright: Notepad++ Portable (SSH root)](https://github.com/marchandd/term_ssh_root_notepadplusplus/ "SSH") 

:checkered_flag: [AbstractSpoon:copyright: ToDoList Portable (SSH root)](https://github.com/marchandd/term_ssh_root_todolist/ "SSH") 

:checkered_flag: [Grimm-Thingamahoochie Software:copyright: WinMerge Portable (SSH root)](https://github.com/marchandd/term_ssh_root_winmerge/ "SSH") 

![Graph4](graph4.gif)

## Usage

[License](LICENSE "License")
