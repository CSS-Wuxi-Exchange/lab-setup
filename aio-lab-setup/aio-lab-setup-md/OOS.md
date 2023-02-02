1.	DC设置
>>![image.png](https://s2.loli.net/2023/01/29/MEVaginc8HkRjfW.png)
>>设置Root Domain。
>>![image.png](https://s2.loli.net/2023/01/29/3yrDEmWMsS7jnc2.png)
>>各台机器加域。
2.	Exchange 2019初始条件准备参考文档。
>>Exchange Server prerequisites,Exchange 2019 system requirements, Exchange 2019 requirements | Microsoft Learn
>>![image.png](https://s2.loli.net/2023/01/29/aDGBLTyFSV6eWuE.png)
以及一些前置组件。
Install-WindowsFeature RSAT-ADDS
Install-WindowsFeature Server-Media-Foundation
Install-WindowsFeature Server-Media-Foundation, NET-Framework-45-Features, RPC-over-HTTP-proxy, RSAT-Clustering, RSAT-Clustering-CmdInterface, RSAT-Clustering-Mgmt, RSAT-Clustering-PowerShell, WAS-Process-Model, Web-Asp-Net45, Web-Basic-Auth, Web-Client-Auth, Web-Digest-Auth, Web-Dir-Browsing, Web-Dyn-Compression, Web-Http-Errors, Web-Http-Logging, Web-Http-Redirect, Web-Http-Tracing, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Lgcy-Mgmt-Console, Web-Metabase, Web-Mgmt-Console, Web-Mgmt-Service, Web-Net-Ext45, Web-Request-Monitor, Web-Server, Web-Stat-Compression, Web-Static-Content, Web-Windows-Auth, Web-WMI, Windows-Identity-Foundation, RSAT-ADDS

重启。
3.	Prepare AD相关。
Prepare Active Directory and domains for Exchange Server, Active Directory Exchange Server, Exchange Server Active Directory, Exchange 2019 Active Directory | Microsoft Learn
>>![image.png](https://s2.loli.net/2023/01/29/GtpNHol6iJ9VbhC.png)
4.	管理员模式运行Exchange安装包，或使用Unattended Mode安装。
E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /mode:Install /r:MB
>>![image.png](https://s2.loli.net/2023/01/29/7UeptdvijYkW5Fq.png)
5.	开始部署OOS。

6.	集成。

New-OfficeWebAppsFarm -InternalURL https://oos.contoso.com -ExternalURL https://oos.contoso.com -CertificateName "Office Online Server Preview Certificate"`

Set-MailboxServer MBX -WacDiscoveryEndpoint https://oos.contoso.com/hosting/discovery

Set-OrganizationConfig -WacDiscoveryEndpoint https://oos.internal.contoso.com/hosting/discovery

Restart-WebAppPool MsExchangeOwaAppPool

Install Office Online Server in an Exchange organization | Microsoft Learn

讨论后偷懒使用http。

New-OfficeWebAppsFarm -InternalURL http://oos.test.com -AllowHttp -EditingEnabled

Set-OrganizationConfig -WacDiscoveryEndpoint http://oos.test.com/hosting/discovery

Set-MailboxServer EX1 -WacDiscoveryEndpoint http://oos.test.com/hosting/discovery

重启IIS。

Reference: https://learn.microsoft.com/en-us/officeonlineserver/deploy-office-online-server

System requirement:
Windows Server 2012 R2, Windows Server 2016 or Windows Server 2019 or Windows Server 2022.
 
Deployment steps:
1.	Install prerequisite software for Office Online Server.
o	Open Microsoft PowerShell prompt as administrator and then run below commands:
Add-WindowsFeature Web-Server,Web-Mgmt-Tools,Web-Mgmt-Console,Web-WebServer,Web-Common-Http,Web-Default-Doc,Web-Static-Content,Web-Performance,Web-Stat-Compression,Web-Dyn-Compression,Web-Security,Web-Filtering,Web-Windows-Auth,Web-App-Dev,Web-Net-Ext45,Web-Asp-Net45,Web-ISAPI-Ext,Web-ISAPI-Filter,Web-Includes,NET-Framework-Features,NET-Framework-45-Features,NET-Framework-Core,NET-Framework-45-Core,NET-HTTP-Activation,NET-Non-HTTP-Activ,NET-WCF-HTTP-Activation45,Windows-Identity-Foundation,Server-Media-Foundation
>>![image.png](https://s2.loli.net/2023/01/29/4gpWQP5HR6Fo3vs.png)

o	Visual C++ Redistributable Packages for Visual Studio 2013

o	Visual C++ Redistributable for Visual Studio 2015

o	Microsoft.IdentityModel.Extention.dll

2.	Install Office online server.

o	Download Office Online Server from VLSC.

o	Run setup.exe
>>![image.png](https://s2.loli.net/2023/01/29/ro5m1eAf79NIZaO.png)
3.	Windows Server 2019 requires Office Online Server July 2021 patch or later. Install November 8, 2022 security update (KB5002276)
>>Description of the security update for Office Online Server: November 8, 2022 (KB5002276) - Microsoft Support
4.	Issue a certificate for OOS
>>![image.png](https://s2.loli.net/2023/01/29/B8KuYZNoSzq9IML.png)
>>![image.png](https://s2.loli.net/2023/01/29/B8KuYZNoSzq9IML.png)
5.	Deploy a single-server Office Online Server farm that uses HTTPS
>>![image.png](https://s2.loli.net/2023/01/29/Asmxdg8boNWt91S.png)