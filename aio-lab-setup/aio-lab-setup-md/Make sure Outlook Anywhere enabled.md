# Make sure Outlook Anywhere enabled

## Configure Outlook Anywhere
**References:**
* [Configure Outlook Anywhere in Exchange 2019](https://www.youtube.com/watch?v=csx2oKYW6G0)
* [Enable-OutlookAnywhere](https://learn.microsoft.com/en-us/powershell/module/exchange/enable-outlookanywhere?view=exchange-ps)
* [How To Configure Active Sync, Outlook Anywhere, Mapi Over Http In Exchange Server 2016](https://www.youtube.com/watch?v=_P2r84GE130)
* [Test-OutlookConnectivity](https://learn.microsoft.com/en-us/powershell/module/exchange/test-outlookconnectivity?redirectedfrom=MSDN&view=exchange-ps)

### Step 1.
Use Exchange PowerShell to run the following command.
```
Enable-OutlookAnywhere -Server:<ServerName> -ExternalHostname:mail.contoso.com -ClientAuthenticationMethod:Ntlm -SSLOffloading:$true
```
Or
```
Set-OutlookAnywhere -Identity “<ExchangeServerName>\RPC (Default Web Site)” -ExternalHostname mail.contoso.com -InternalHostname mail.contoso.com -ExternalClientsRequireSsl $true -InternalClientsRequireSsl $true -DefaultAuthenticationMethod NTLM
```
![Screenshot _520_.png](https://s2.loli.net/2022/09/20/L96c8VBU5nNkxiD.png)


### Step 2.
To verify configuration, run the following command.
```
Get-OutlookAnywhere | Select Server,ExternalHostname,Internalhostname | fl
```
![Screenshot _521_.png](https://s2.loli.net/2022/09/20/OMi6TWIuyDzmHjf.png)


### Step 3.
login to Exchange Admin Center and select the 'Servers' tab, select 'Servers', select \<ServerName\> and then select the 'Edit' button.
![Screenshot _522_.png](https://s2.loli.net/2022/09/20/sXr7vtyaZBVmjK3.png)

### Step 4.
Left side Select 'Outlook Anywhere', Type Internal & External URL, under when connecting to your organization select 'NTLM' and then click on 'Save'.
![Screenshot _523_.png](https://s2.loli.net/2022/09/20/u7XnOSr6y8FD9eM.png)
