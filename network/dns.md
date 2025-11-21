# DNS workaround

Hosts file,DNS cache,DNS server,LLMNR,NetBIOS,WINS

Resolve-DnsName lon-dc1 -DnsOnly
Set-NetLlmnr -Status Disabled
nbtstat -a lon-dc1