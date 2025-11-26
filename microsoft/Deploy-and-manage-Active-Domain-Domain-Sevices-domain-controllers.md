# 1. Intro
-  foundation for enterprise networks that run Windows and non-Windows 
- The AD DS database is the central store of all the domain objects

# 2. Define AD DS
GC:A copy of all objects and `some of their attributes` from all domains in an AD DS forest

# 3. Define AD DS forest and domain
- tree {common root, common schema, global catalog}[security boundary, replication boundary], group {users groups, computers} [replication boundary, administrative unit]
Contoso.com Forest
|--Contoso domain tree
|--Tailspin Toys domain tree
|--Fabrikam domain tree


# 4. Deploy AD DS DC
- When you create the first domain controller for a domain, you must specify the NetBIOS name for the domain.
- [C:\Windows\NTDS, C:\Windows\SYSVOL]
- update method 'best practice': Add servers in a existing domain.

# 5. Migrate a DC to a new site
- create site, map to subnet

# 6. Manage AD DS operations masters

- Get-ADDomai, Get-ADForest
netdom query fsmo
[regsvr32 schmmgmt.dll, mmc]
ntdsutil

