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
