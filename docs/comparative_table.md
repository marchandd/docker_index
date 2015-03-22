# Comparative efficiency approach to provide Docker GUI Virtual Environments dedicated to facilitate Windows/Linux cross-over usage

Return to [index](https://github.com/marchandd/docker_index "Index")

## Studies with focus on domains differences

### Diversity of method differences to produce GUI VE to access to Firefox

| marchandd/Docker image | Account | Remote | Windows | Security | Size  
| --- | --- | --- | --- | --- | ---   
| term_x11shared_sudoers_firefox | sudoers | - | - | - | 450 Mb  
| vncxvfb_wine_firefox | root | - | Windows | VNC basic | 1250 Mb  
| term_ssh_root_firefox | root | Remote | Windows | SSH | 450 Mb  
| term_ssh_user_firefox | non root | Remote | Windows | SSH | 450 Mb  

### Mono environment to make possible to run Console or Gtk applications

Common Local/Remote access on Linux/Windows target with SSH Security.

| marchandd/Docker image | Account | Software | Size  
| --- | --- | --- | ---   
| term_ssh_root_mono | root | Mono simple | 400 Mb  
| term_ssh_user_monodotnet45 | non root | Mono complete | 950 Mb  
| term_ssh_user_monodevelop | non root | Mono complete & Editor | 1050 Mb  

### Windows Portable-apps grouped samples running with Wine emulator

Common root account on Linux/Windows target with SSH Security including Wine.

| marchandd/Docker image | Remote | Security | Software | Size  
| --- | --- | --- | --- | ---   
| vncxvfb_wine_portableapps | - | VNC | 5 Portable-Apps | 1300 Mb  
| term_ssh_root_wine | Remote | SSH | - | 1250 Mb  
| term_ssh_wine_portableapps | Remote | SSH | 5 Portable-Apps | 1300 Mb  

### Windows Portable-apps dedicated samples running with Wine emulator

Common root account to Local/Remote access on Linux/Windows target with SSH Security including Wine.

| marchandd/Docker image | Ext | Software | Version | Size  
| --- | --- | --- | ---   
| term_ssh_wine_antrenamer | EXE | antrenamer | Last | 1250 Mb  
| term_ssh_wine_freecommander | EXE | freecommander | Old | 1250 Mb  
| term_ssh_wine_notepadplusplus | EXE | notepadplusplus | Last | 1250 Mb  
| term_ssh_wine_todolist | ZIP | todolist | Last | 1250 Mb  
| term_ssh_wine_winmerge | EXE | winmerge | Last | 1250 Mb  
| term_ssh_wine_7zip | EXE | 7-Zip | Last | 1250 Mb  
 
## All Studies together

| marchandd/Docker image | Account | Remote | Windows | Security | Wine | Software | Version | Size  
| --- | --- | --- | --- | --- | --- | --- | ---  
| term_x11shared_sudoers_firefox | sudoers | - | - | - | - | - | - | 450 Mb  
| vncxvfb_wine_firefox | root | - | Windows | VNC | Wine | - | - | 1250 Mb  
| term_ssh_root_firefox | root | Remote | Windows | SSH | - | - | - | 450 Mb  
| term_ssh_user_firefox | non root | Remote | Windows | SSH | - | - | - | 450 Mb  
| term_ssh_root_mono | root | Remote | Windows | SSH | - | Mono simple | Last | 400 Mb  
| term_ssh_user_monodotnet45 | non root | Remote | Windows | SSH | - | Mono complete | Last | 950 Mb  
| term_ssh_user_monodevelop | non root | Remote | Windows | SSH | - | Mono complete & Editor | Last | 1050 Mb  
| vncxvfb_wine_portableapps | root | - | Windows | SSH | Wine | 5 Portable-Apps | - | 1300 Mb  
| term_ssh_root_wine | root | Remote | Windows | SSH | Wine | - | - | 1250 Mb  
| term_ssh_wine_portableapps | root | Remote | Windows | SSH | Wine | 5 Portable-Apps | - | 1300 Mb  
| term_ssh_wine_antrenamer | root | Remote | Windows | SSH | Wine | 1 Portable-App | Last | 1250 Mb  
| term_ssh_wine_freecommander | root | Remote | Windows | SSH | Wine | 1 Portable-App | Old | 1250 Mb  
| term_ssh_wine_notepadplusplus | root | Remote | Windows | SSH | Wine | 1 Portable-App | Last | 1250 Mb  
| term_ssh_wine_todolist | root | Remote | Windows | SSH | Wine | 1 Portable-App | Last | 1250 Mb  
| term_ssh_wine_winmerge | root | Remote | Windows | SSH | Wine | 1 Portable-App | Last | 1250 Mb  
| term_ssh_wine_7zip | root | Remote | Windows | SSH | Wine | 1 Portable-App | Last | 1250 Mb  
