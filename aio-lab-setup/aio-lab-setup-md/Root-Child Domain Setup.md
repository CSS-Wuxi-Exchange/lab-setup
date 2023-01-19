# Root-Child Domain Setup
## Root Domain
1. 部署4台VM：DC01;EX01;DC02;EX02
2. 登录DC01，打开Server Manager，右上角选择Add Roles and Features
>>![2.jpg](https://s2.loli.net/2023/01/16/SKBplgmYEMT2aNw.jpg)
3. 选择Role-based or feature-based installation
>>![3.jpg](https://s2.loli.net/2023/01/16/HqQjmJWpiaBodGP.jpg)
4. 选择DC01
>>![1.4.jpg](https://s2.loli.net/2023/01/20/7myKSwcDjtBlgo2.jpg)
5. 添加Active Directory Domain Services
>>![1.5.jpg](https://s2.loli.net/2023/01/20/24KEYSVdcJRrfot.jpg)
6. 全部默认下一步进行安装
7. 在Server Manager中点击右上角，Promote this server to a domain controller
>>![1.7.jpg](https://s2.loli.net/2023/01/20/XT6hvPbO3U5sFLV.jpg)
8. 选择add a new forest并填入父域名，下一步
>>![1.8.jpg](https://s2.loli.net/2023/01/20/Z2iVqdQmlcuAChL.jpg)
9. 创建DSRM密码，下一步
>>![1.9.jpg](https://s2.loli.net/2023/01/20/NvWk9HMSnJyP5Ap.jpg)
10. 全部默认下一步进行安装
11. 等待AD进行配置，使用新创建的域重新登录DC01

## Child Domain
1. 登录准备部署子域的DC02
2. 打开网卡设置，双击打开，选择Properties，选择IPV4，将DC01的IP地址填入DNS服务器，IP地址网关等填写本机默认
>>![2.2.jpg](https://s2.loli.net/2023/01/20/IvZFtXcTA9s5SOp.jpg)
3. 打开设置，导航至System -> About -> Join a domain
>>![2.3.jpg](https://s2.loli.net/2023/01/20/TuieOf2PzdHvNJ9.jpg)
4. 输入父域域名并登陆父域管理员账号
5. 在本机上添加父域管理员账号并重启电脑完成加父域
>>![2.5.jpg](https://s2.loli.net/2023/01/20/lepYTwrVO6NtFc9.jpg)
6. 使用父域管理员账号登陆DC02
7. 打开Server Manager，右上角选择Add Roles and Features
>>![2.7.jpg](https://s2.loli.net/2023/01/20/xsL21mHJCVw6KSy.jpg)
8. 选择Role-based or feature-based installation
>>![2.8.jpg](https://s2.loli.net/2023/01/20/bJuGtyvP1V5Cc6r.jpg)
9. 选择DC01
>>![1.4.jpg](https://s2.loli.net/2023/01/20/7myKSwcDjtBlgo2.jpg)
10. 添加Active Directory Domain Services
>>![1.5.jpg](https://s2.loli.net/2023/01/20/24KEYSVdcJRrfot.jpg)
11. 全部默认下一步进行安装
12. 在Server Manager中点击右上角，Promote this server to a domain controller
>>![1.7.jpg](https://s2.loli.net/2023/01/20/XT6hvPbO3U5sFLV.jpg)
13. 选择add a new domain to an existing forest，选择child domain，填入子域域名
>>![2.13.jpg](https://s2.loli.net/2023/01/20/2dekEzVbatuUN3M.jpg)
14. 创建DSRM密码，下一步
>>![1.9.jpg](https://s2.loli.net/2023/01/20/NvWk9HMSnJyP5Ap.jpg)
15. 全部默认下一步进行安装

## Join Domain
1. 登陆EX01
2. 打开网卡设置，双击打开，选择Properties，选择IPV4，将DC01的IP地址填入DNS服务器，IP地址网关等填写本机默认
>>![2.2.jpg](https://s2.loli.net/2023/01/20/IvZFtXcTA9s5SOp.jpg)
3. 打开设置，导航至System -> About -> Join a domain
>>![2.3.jpg](https://s2.loli.net/2023/01/20/TuieOf2PzdHvNJ9.jpg)
4. 输入父域域名并登陆父域管理员账号
5. 在本机上添加父域管理员账号并重启电脑完成加父域
>>![2.5.jpg](https://s2.loli.net/2023/01/20/lepYTwrVO6NtFc9.jpg)
6. 登陆EX02
7. 打开网卡设置，双击打开，选择Properties，选择IPV4，将DC02的IP地址填入DNS服务器，IP地址网关等填写本机默认
>>![2.2.jpg](https://s2.loli.net/2023/01/20/IvZFtXcTA9s5SOp.jpg)
8. 打开设置，导航至System -> About -> Join a domain
>>![2.3.jpg](https://s2.loli.net/2023/01/20/TuieOf2PzdHvNJ9.jpg)
9. 输入子域域名并登陆子域管理员账号
10. 在本机上添加子域管理员账号并重启电脑完成加子域
>>![2.5.jpg](https://s2.loli.net/2023/01/20/lepYTwrVO6NtFc9.jpg)

## Prerequisites
1. 登陆全部服务器
2. 下载并安装NET4.8
>>https://download.visualstudio.microsoft.com/download/pr/014120d7-d689-4305-befd-3cb711108212/0fd66638cde16859462a6243a4629a50/ndp48-x86-x64-allos-enu.exe

3. 下载并安装VC++ 2013
>>https://aka.ms/highdpimfc2013x64enu

4. 下载并安装IIS URL Rewrite Module
>>https://www.iis.net/downloads/microsoft/url-rewrite

5. 下载并安装Microsoft Unified Communications Managed API 4.0, Core Runtime 64-bit
>>https://www.microsoft.com/download/details.aspx?id=34992

6. EX服务器使用PowerShell运行以下命令
>>Install-WindowsFeature NET-Framework-45-Features, Server-Media-Foundation, RPC-over-HTTP-proxy, RSAT-Clustering, RSAT-Clustering-CmdInterface, RSAT-Clustering-Mgmt, RSAT-Clustering-PowerShell, WAS-Process-Model, Web-Asp-Net45, Web-Basic-Auth, Web-Client-Auth, Web-Digest-Auth, Web-Dir-Browsing, Web-Dyn-Compression, Web-Http-Errors, Web-Http-Logging, Web-Http-Redirect, Web-Http-Tracing, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Lgcy-Mgmt-Console, Web-Metabase, Web-Mgmt-Console, Web-Mgmt-Service, Web-Net-Ext45, Web-Request-Monitor, Web-Server, Web-Stat-Compression, Web-Static-Content, Web-Windows-Auth, Web-WMI, Windows-Identity-Foundation, RSAT-ADDS

7. 在所有服务器上下载Exchange镜像，并用PowerShell挂载
>>Mount-DiskImage -ImagePath C:\ExchangeServer2016-x64-CU23.ISO

## Installation
1. 在主DC上运行prepare ad
>>E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareAD /OrganizationName:"TestOrg"
2. 在主DC上运行prepare schema
>>E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareSchema
3. 在主DC上运行prepare 主domain
>>E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareDomain:root.com
4. 在主DC上打开ADUC，找到以下的组并将子域admin添加为成员，添加后需要重新logon生效
>>Enterprise Admins; Schema Admins; Organization Management
5. 在子DC上运行prepare 子domain
>>E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareDomain:child.root.com
6. 重启所有服务器
7. 打开父域的ADUC，找到Enterprise Admins; Organization Management; Schema Admins组，添加子域管理员为成员
>>![5.7.jpg](https://s2.loli.net/2023/01/20/Iqc1VxblNgDBrva.jpg)
8. 根据各自Ex服务器所属的域，指定对应DC进行安装
>>E:\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /mode:Install /role:Mailbox /DomainController:DCxx