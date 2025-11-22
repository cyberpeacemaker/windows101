# Notification
Win + A / Win + N

# NTFS

 - NTFS (New Technology File System or simply)
    - FAT16/FAT32 (File Allocation Table) 
    - HPFS (High Performance File System)

- file system  
![file system](./img/image.png)

| Permission          | Meaning for Folders                                                                 | Meaning for Files                                                       |
|---------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **Read**            | Permits viewing and listing of files and subfolders                                 | Permits viewing or accessing the file's contents                        |
| **Write**           | Permits adding of files and subfolders                                               | Permits writing to a file                                               |
| **Read & Execute**  | Permits viewing and listing of files and subfolders as well as executing of files; inherited by files and folders | Permits viewing and accessing the file's contents as well as executing the file |
| **List Folder Contents** | Permits viewing and listing of files and subfolders as well as executing of files; inherited by folders only | N/A                                                                     |
| **Modify**          | Permits reading and writing of files and subfolders; allows deletion of the folder   | Permits reading and writing of the file; allows deletion of the file    |
| **Full Control**    | Permits reading, writing, changing, and deleting of files and subfolders             | Permits reading, writing, changing, and deleting of the file            |

# ADS
The command to view ADS using Powershell: `Get-Item -Path file.exe -Stream *`
https://www.malwarebytes.com/blog/101/2015/07/introduction-to-alternate-data-streams



# EFS
https://learn.microsoft.com/en-us/windows/win32/fileio/file-encryption
Encryption File System

# System Variables
%windir% 
- operating system path
- the number of processors used by the operating system
- the location of temporary folders 
- System32 folder holds the important files that are critical for the operating system.

# User Accounts
lusrmgr.msc (Local User and Group Management. )


- Administrator
- Standard User

 user's profile is done upon initial login
![alt text](./img/image-1.png)

# UAC


# Setting, Control Panel
control

# Task Manager
Ctrl+SHIFT+Esc