# AD DS
The AD DS database is the central store of all the domain objects, such as user accounts, computer accounts, and groups. 

- Logical Components: Partition, Schema, Domain, Domain tree, Forest, OU, Container
- Physical component: Domain Controller, Data store, Global catalog server, Read-only domain controller, site, subnet

- C:/Windows/NTDS, C:/Windows/SYSVOL

> Which component of AD DS is responsible for storing a read-only copy of all objects in a multi-domain forest? 
>A **Global Catalog server** stores:

* **A *partial* attribute set (PAS)** for *every* object in the forest (from all domains)
  → This includes only selected attributes that are useful for searching and locating objects (e.g., names, group memberships, email addresses).
* **A *full* attribute set** for all objects in the domain where the GC is also a domain controller.

---

# User, Group, Computer
account

## User
- People (employee) [Administrator, Standard user]
- Local Service Accounts [built-in Service, Network Service, Local System], MSA(Managed service account)
- gMSA(gourp MSA), dMSA(Delegated MSAA)

>1. A service running on multiple servers in a Windows Server domain needs to use the same service account. Which type of service account should you deploy to ensure security and ease of management? 
>dMSA prevents credential harvesting by binding authentication to device identity.

## Computer

- They have an account with a sign-in name and password that Windows changes automatically on a periodic basis.
- They authenticate with the domain.
- They can belong to groups and have access to resources, and you can configure them by using Group Policy.
s, [Local, Domain-local, Global, Universal]

## Group

- type, [Security, Distribution]
- scope

---

# Forest and Domain

- Forest {common root, common schema, global catalog} schema master role, domain naming master role, Enterprise admins group, schema admins group}
    - security boundary, replication boundary

- Domain {Users, Groups, Computers}, {RID master role, infrastructure role, PDC emulator master role, Domain admins group}
    - replication boundary, administrative unit

- Trust {parent-and-child, tree-root, extrenal, realm, forest, shortcut}

---

# OU

>OU for: GPO, Delegation
>Gruop for: file share permission, access

- consolidate, delegate, - COM+, view > advanced features

>OUs are the modern, flexible container type; “containers” exist mainly for legacy reasons and a few technical behaviors.

---

# Managiing

---

# SN

## Partial Attribute Set
adsiedit.msc
Get-ADObject -SearchBase (Get-ADRootDSE).schemaNamingContext `
  -LDAPFilter "(isMemberOfPartialAttributeSet=TRUE)" -Properties lDAPDisplayName |
  Select-Object lDAPDisplayName
