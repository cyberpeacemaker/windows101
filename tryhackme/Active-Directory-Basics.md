# 1.Introduction
Microsoft's Active Directory is the backbone of the corporate world.

# 2.Windows Domain
Windows domain is a group of users and computers under the administration of a given business.

- Active Directory (AD):centralise the administrationin a single repository called . 
- Domain Controller (DC): The server that runs the Active Directory services

# 3.Active Domain
Core: AD Domain Service(AD DS), which holds the information of all of the "objects" that exist on your network.

- Users: security principals, can be authenticated and can be assigned privileges over resources , [People, Services]
- Machines: a machine named `DC01` will have a machine account called `DC01$`.

- Groups [Security, Distribution]

- OU: Policy (A user can only be a part of a single OU at a time.)
- Group: Persmissions over resources.

# 4.Managing Users in AD

- Delete OU (view > advanced features > protect object from accidental deletion) 
EX: IT Support granted permission for reset password

# 5.Managins Computers in AD

- Workstations: This is the device they will use to do their work or normal browsing activities. These devices should never have a privileged user signed into them.

# 6.Policy

GPO > [linked OU , any sub-OUs under]
GPOs are distributed to the network via a network share called SYSVOL, C:\Windows\SYSVOL\sysvol\

- users or computers
- scope [links, security filter]

> pgupdate /force

# 7.

# 8. Tree, Forest, Trust

- Tree: domains that share the same namespace 
- Forest: The union of several trees with different namespaces into the same network 
- Trust (trust➡, access⬅), doesn't automatically grant access to all resources on other domains. Once a trust relationship is established, you have the chance to authorise users across different domains

# 9.
Active Directory Hardening Room, Compromising Active Directory module 
