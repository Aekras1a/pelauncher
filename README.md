# pelauncher [![Build status](https://ci.appveyor.com/api/projects/status/1b7qta0rs4bwtpho?svg=true)](https://ci.appveyor.com/project/feel-the-dz3n/pelauncher)
 Portable Executable launcher for Windows NT
 
![image](https://user-images.githubusercontent.com/25367511/63372070-0d742a80-c38e-11e9-8e97-7315d41aa8d4.png)

# What is this?
This program allows to run any portable executable avoiding Windows checks. Examples:
 - I can start any Windows CE application (with [WCECL](https://github.com/feel-the-dz3n/wcecl)) without editing executable. Windows will not check for subsystem;
 - Once I tried to start x86 Windows Longhorn 4074 kernel, which failed because HAL.dll and other libraries are not found;
 
   ![image](https://user-images.githubusercontent.com/25367511/63372394-a86d0480-c38e-11e9-934c-f6a2d361146a.png)
   
 - Windows 10 refuses to launch Windows XP setup (``winnt32.exe``), but this program allows. For some reason, setup fails because ``winnt32u.dll`` is not found, even if it exists. Maybe Windows blocks and LoadLibrary calls for this;
 - Also it can run native NT applications. Over Win32 subsystem. Even if they are x86 on x64 system. I tried to start ``smss.exe`` from ReactOS and it crashed my x64 Windows 10;
 - Also it avoid machine check, so it starts even ARM software.

# Requirements
 - Minimal OS version: Windows XP (not tested);
 - Recommended OS version: Windows 10;
 - Only x86. There are ARM and x64 builds, but they are broken.
 
# Build
Visual Studio 2017 was used to create this project.

# Credits
 - [This](https://stackoverflow.com/questions/48981582/running-portable-executable-in-memory-using-the-winapi-c-programming) question on Stackoverflow
 - [Yaroslav Kibysh](https://github.com/feel-the-dz3n)
 