**DSC TO INSTALL IIS**
```
configuration IISInstall
{
Node “localhost”
{
WindowsFeature IIS
{
Ensure = “Present”
Name = “Web-Server”
} } }
```

**Powershell Command for IIS**
```
Install-WindowsFeature -name Web-Server -IncludeManagementTools
```



```sh
New-NetFirewallRule –DisplayName "Allow ICMPv4-In" –Protocol ICMPv4
```

Azure routes traffic between all subnets within a virtual network, by default

```
https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-create-route-table-portal
```
Port 445
```
New-NetFirewallRule -DisplayName "Port 445" -Direction Inbound -LocalPort 445 -Protocol TCP -Action Allow
```
open icmp port windows 
```
# For IPv4
netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol="icmpv4:8,any" dir=in action=allow
 
#For IPv6
netsh advfirewall firewall add rule name="ICMP Allow incoming V6 echo request" protocol="icmpv6:8,any" dir=in action=allow
```
