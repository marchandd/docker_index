# Docker:copyright: GUI Virtual Environment Proof of concept Studies

## Goal

Proof of concept was started for my job to reduce cost licence on Windows system and I choosen to accentuate by myself.  
The goal of this approach is to provide Docker GUI Virtual Environments (VE) dedicated to facilitate Windows/Linux cross-over usage.  
Allow Linux users who want to use a Windows application to run under Wine without the problems of version compatibility or graphics drivers.  
I wanted to focus on solutions dedicated to Mono/Dotnet and Portable-Apps.

Studies are splitted into three domains : 
- Diversity of method differences to produce GUI VE to access to Firefox. Choose the most better solutions for the other studies.  
- Mono environment to make possible to run Console or Gtk applications.
- Windows Portable-apps (grouped or dedicated samples) running with Wine emulator.
 
SSH is more efficient ways but experiment by yourself all approaches studies with the links below for Docker images.

### Mozilla Firefox (4 ways)

Last version of Mozilla Firefox ready to use.

:checkered_flag: [X11shared (sudoers)](https://github.com/marchandd/term_x11shared_sudoers_firefox/ "X11shared") but dangerous access permissions... 

:checkered_flag: [VNC (root with xvfb & wine)](https://github.com/marchandd/vncxvfb_wine_firefox/ "VNC") with VNC protocol but not crypted... 

Remote access and more secure with SSH protocol:

:checkered_flag: [SSH (root)](https://github.com/marchandd/term_ssh_root_firefox/ "SSH") 

:checkered_flag: [SSH (non root user)](https://github.com/marchandd/term_ssh_user_firefox/ "SSH") 

![Graph1](graph1.gif)

### Mono Environment (2 ways) and Mono Editor (1 VE)

Since [Microsoft announced 11.12.2014](http://news.microsoft.com/2014/11/12/microsoft-takes-net-open-source-and-cross-platform-adds-new-development-capabilities-with-visual-studio-2015-net-2015-and-visual-studio-online/ "Microsoft announce"), .NET and Visual Studio Community are committed to supporting free and cross-platform, Mono won to be discovered in a Linux environment.  

Last version of Mono environment ready to be exploited for Mono app with SSH (more efficient).

:checkered_flag: [Mono Docker official (SSH root)](https://github.com/marchandd/term_ssh_root_mono/ "SSH") A Docker official version but not mono-complete. 

:checkered_flag: [Xamarin:copyright: Mono-complete install (SSH user)](https://github.com/marchandd/term_ssh_user_monodotnet45/ "SSH") To have mono-complete install with last versions.

Last version of Mono environment IDE ready to use with SSH (more efficient).

:checkered_flag: [Xamarin:copyright: MonoDevelop IDE (SSH user)] (https://github.com/marchandd/term_ssh_user_monodevelop/ "SSH")

![Graph2](graph2.gif)

### Grouped samples Windows Portable-apps (2 ways)

Since 2013 buzz with Docker technology and since 2014 with Microsoft announcement to support free and cross-platform, and because I like Linux and Windows, that give me the idea to emulate Windows apps in Linux environment.  
This is the reason why I searched an easy and reproductible method to propose Portable-apps and now that is working I let you try by yourself.  
[My Portable-apps approach explained but not boring !](https://github.com/marchandd/docker_index/blob/master/docs/portable-apps.md "Portable-apps")

Windows Portable-apps grouped samples easy to install, update and use with VNC.

:checkered_flag: [Windows Portable-apps samples (VNC)](https://github.com/marchandd/vncxvfb_wine_portableapps/ "VNC") 

To prove than this method can be reproductible, Windows Portable-apps samples easy to install, update and use with SSH (more efficient).

:checkered_flag: [Wine (SSH root)](https://github.com/marchandd/term_ssh_root_wine/ "SSH")

:checkered_flag: [Windows Portable-apps samples (SSH root)](https://github.com/marchandd/term_ssh_wine_portableapps/ "SSH")

![Graph3](graph3.gif)

### Dedicated samples Windows Portable-app (6 VE)

A declination of the more efficient of reproductible method for Windows Portable-apps grouped samples, Windows Portable-apps dedicated samples easy to install last version directly (except for FreeCommander) and use with SSH.  
:star2: Very easy way that take less than 5 minutes, you just have to run only 3 times one same command in cyclic mode to run sub programs and just 1 command line to active alias !

:checkered_flag: [Antp.be:copyright: AntRenamer Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_antrenamer/ "SSH") 

:checkered_flag: [Marek Jasinski:copyright: FreeCommander Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_freecommander/ "SSH")  

:checkered_flag: [Notepad++Team:copyright: Notepad++ Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_notepadplusplus/ "SSH") 

:checkered_flag: [AbstractSpoon:copyright: ToDoList Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_todolist/ "SSH") 

:checkered_flag: [Grimm-Thingamahoochie Software:copyright: WinMerge Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_winmerge/ "SSH") 

Another way to prove than this method can be reproductible for Windows Portable-apps, new Portable-app (not included in grouped samples) running with the same adaptation concept just replacing some variables values in scripts headers.

:checkered_flag: [7-Zip developers:copyright: 7-Zip Portable (SSH root)](https://github.com/marchandd/term_ssh_wine_7zip/ "SSH") 

![Graph4](graph4.gif)

## Virtual Environment usage documentations

[My Portable-apps explained approach very interesting way (not boring !)](https://github.com/marchandd/docker_index/blob/master/docs/portable-apps.md "Portable-apps")

[Comparative table](https://github.com/marchandd/docker_index/blob/master/docs/comparative_table.md "Comparison")

[Test environments](https://github.com/marchandd/docker_index/blob/master/docs/test_environments.md "Tests")

[GUI Virtual Environment Studies Docker images preparation on Linux Ubuntu](https://github.com/marchandd/docker_index/blob/master/docs/ubuntu_docker.md "Ubuntu Docker install")

[GUI Virtual Environment Studies Docker images preparation on Microsoft Windows](https://github.com/marchandd/docker_index/blob/master/docs/windows_docker.md "Windows Docker install")

[Frequently asked questions](https://github.com/marchandd/docker_index/blob/master/docs/faq.md "FAQ")

[Open-source license](LICENSE "License")
