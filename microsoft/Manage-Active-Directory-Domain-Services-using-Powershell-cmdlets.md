# 1. Intro
The AD DS database stores information about the objects that are part of the network environment, such as accounts for users, computers, and groups. 
The AD DS database is `searchable` and provides a mechanism for `applying configuration` and security settings for all of those objects.

# 2. User account in PowerShell

- SAM account name, distinguished name
> -Filter * -Properties *

> ! Windows PowerShell only returns **a default set** of properties when you use Get-ADUser. use the **-Properties** parameter with a comma-separated list of properties or the **“*” wildcard**.

# 3. Group in PowerShell

- group, principalgroupmembership

# 4. Computer account in Powershell

- Test-ComputerSecureChannel, Reset-ComputerMachinePassword

# 5. OU in PowerShell

- organizationalunit
- New-ADObject -Name "AnaBowmancontact" -Type contact