# disable-MAX_PATH-in-windows-10

DISABLES MAX_PATH (260 CHARS) IN WINDOWS-10 (VERSION 1607 AND LATER)

Right click "LongPathsEnabled.reg" -> Merge

Ref. https://msdn.microsoft.com/en-us/library/windows/desktop/aa365247(v=vs.85).aspx#maxpath
Quoted from above ref. link:

Starting in Windows 10, version 1607, MAX_PATH limitations have been removed from common Win32 file and directory functions.

A registry key allows you to enable or disable the new long path behavior. To enable long path behavior set the registry key at HKLM\SYSTEM\CurrentControlSet\Control\FileSystem LongPathsEnabled (Type: REG_DWORD). The key's value will be cached by the system (per process) after the first call to an affected Win32 file or directory function (list follows). The registry key will not be reloaded during the lifetime of the process. In order for all apps on the system to recognize the value of the key, a reboot might be required because some processes may have started before the key was set.
The registry key can also be controlled via Group Policy at Computer Configuration > Administrative Templates > System > Filesystem > Enable NTFS long paths.
