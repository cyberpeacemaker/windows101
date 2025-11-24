# 1. Intro

AD DS Tutor (https://aka.ms/ADDSAppliedSkillTutor)

# 2. Users, groups, computers

Group managed service accounts enable you to extend the capabilities of standard managed service accounts to more than one server in your domain.

Standard managed service accounts can't provide managed service account functionality to services that are running on more than one server. 

By using group managed service accounts, you can configure multiple servers to use the same managed service account and still retain the benefits that managed service accounts provide
EX: automatic password maintenance and simplified SPN management.

# 7. Bulk Managements
Get-ADUser -Filter {city -eq "London"} | ForEach-Object {
Move-ADObject -Identity $_.DistinguishedName -TargetPath "OU=London,DC=adatum,DC=com"
}

# 8. Maintain AD DS

- best practice: an AD DS domain should have at least two domain controllers per AD DS site. 
- recycle bin
- backup and restore, DSMR, [Nonauthoritative, Authoritative]