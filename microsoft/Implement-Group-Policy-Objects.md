# 2. GPO
GPO is an object that contains one or more policy settings that apply to one or more configuration settings for a user or a computer.

- starter GPOs, [export/import from cabinet (.cab), SYSVOL]

# 3. Scope & Inheritance
Resultant Set of Policies (RSoPs) for a user or computer will be the cumulative effect of site, domain, and OU policies.

- [scope, linking], filter [security, WMI] (select * from Win32_OperatingSystem where Version like "10.%")
- order [local < Site-linked < Domain < OU < Child OU], specified on 'Linked Group Policy Objects' tab
- disbale the link, disable {user, computer} configuration
- bllock inheritance, enforced

>Group Policy Inheritance doesn't account for policies that are linked to a site, for GPO security, or WMI filtering.
>! Sites

# 4. Domain-based GPO
local GPOs, which are primarily used when computers aren't connected to domain environments.l

You shouldn't add unrelated policy settings to `Default Domain Policy` GPO. If you need to configure other settings to apply broadly in your domain, create additional GPOs that link to the domain.

# 5. Configure GPO

- RSoP is the net effect of GPOs [GP Results Wizard, GP Modeling Wizard, GPResult.exe]

# 6. GPO Storage
GPO actually includes two components.

- GP container (directory part of a GPO), GP template (in SYSVOL)

Get-ADObject -SearchBase "CN=Policies,CN=System,DC=Adatum,DC=com" -LDAPFilter "(objectClass=groupPolicyContainer)" -Properties *

- Replication [DRA, DFSR],  Group Policy container will replicate to a domain controller first.

# 7. Administrative Templates
administrative templates result in changes to the registry. using a registry-based policy is the simplest and best way. 
All the settings in the Administrative Templates node of a GPO are stored in files.

- HKEY_LOCAL_MACHINE, HKEY_CURRENT_USER, conflicting settings, the computer setting prevails.
- C:\Windows\PolicyDefinitions > \\FQDN\SYSVOL\FQDN\Policies (Central Store)
- admx, adml

> The IT department in Adatum is deploying a new version of Microsoft Office in their on-premises environment. The administrator wants to configure settings with GPOs for Office. What should they do?