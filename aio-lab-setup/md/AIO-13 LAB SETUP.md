# AIO-13 LAB SETUP

## Overview


**References:**

- [Exchange 2013 prerequisites: Exchange 2013 Help | Microsoft Docs](https://docs.microsoft.com/en-us/exchange/exchange-2013-prerequisites-exchange-2013-help#windows-server-2012-r2-and-windows-server-2012-prerequisites)
- [Prepare Active Directory and domains](https://learn.microsoft.com/en-us/exchange/prepare-active-directory-and-domains-exchange-2013-help)

| **EX13_AIO** |     |     |
| --- | --- | --- |
| Host | shgbsvmas | [VMAS - Workspaces](https://shgbsvmas/#/Workspaces) |
| Host Name | AIO-13 |     |
| Role | DC & CAS & MBX & Outlook |     |
| OS Version | Windows Server 2012 R2 Datacenter |     |
| Original OS Language | English (en-us) |     |
| Additional Language Packs | Simplified Chinese (zh-cn)<br>Traditional Chinese (zh-tw) |     |
| Exchange Build Number | CU23 | Exchange Server build numbers and release dates<br>[https://docs.microsoft.com/en-us/exchange/new-features/build-numbers-and-release-dates?view=exchserver-2019](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fexchange%2Fnew-features%2Fbuild-numbers-and-release-dates%3Fview%3Dexchserver-2019&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=KP6Ut9En9lE7r7O5K4WpgyqFWTr%2BTZlC7kEsCGCW3E8%3D&reserved=0) |
| Password Complexity | 1   |     |
| Certificate created and configured | Exchange self-generated |     |
| Outlook Version | Microsoft 365 2019 |     |
| Outlook Language Packs | Simplified Chinese (zh-cn)<br>English (en-us)<br>Traditional Chinese (zh-tw) |     |
| Outlook Anywhere enabled | Y   |     |
| OAB and EWS enabled | Y   |     |
| Network Monitor installed | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Fiddler installed | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Telnet25 | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| ExTRA | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Disable CRL check |     | Exchange 2010 Management Console (EMC) is very slow<br>[https://blogs.technet.microsoft.com/nawar/2011/06/03/exchange-2010-management-console-emc-is-very-slow/](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fblogs.technet.microsoft.com%2Fnawar%2F2011%2F06%2F03%2Fexchange-2010-management-console-emc-is-very-slow%2F&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=Hoo%2BgXCBkwvIWsFNDVQY9bxiem7vrN7qi8xtOVm8nvo%3D&reserved=0)<br>Configuring Exchange Servers Without Internet Access<br>[https://techcommunity.microsoft.com/t5/exchange-team-blog/configuring-exchange-servers-without-internet-access/ba-p/593692](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftechcommunity.microsoft.com%2Ft5%2Fexchange-team-blog%2Fconfiguring-exchange-servers-without-internet-access%2Fba-p%2F593692&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=%2BD6NVy2WMbhC%2FmJJ6Un5dwzDGw2gu1nEQ%2BnqjMLeXwY%3D&reserved=0) |
| NIC | Private IP |     |
| ActiveSync device connectivity | Y   |     |
| Additional disk for Backup issue | Y   |     |
| Enable Windows Server Backup | Y   |     |
| Backup | Y   |     |
| Snap Shot | Y   |     |
| Lab known issue |     | If EMC and EMS does not work properly, please clean the credential manager in the Control Panel. It is because Outlook user credential cache. |
| FAQ |     |     |

* * *

## Deployment Step by step


The following steps are required in the deployment of AIO-13. The same steps on AIOs are not mentioned here, for more information about parent documentation, see [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).

### Step 1: configure the all-in-one virtual machine on VMAs.

**Attention**: the OS version is Windows Server 2012 R2 Datacenter.

<img src="https://s2.loli.net/2022/09/15/Iy2nvVaxgNKkUPt.png" alt="13-sp-1.png" width="693" height="514" class="jop-noMdConv">

### Step 2: log on to the AIO with RDCMan.exe.

**Attention**: login "other user". Username: contoso\\administrator; Password: 1.

<img src="https://s2.loli.net/2022/09/15/JI72AKnwlTktgeo.png" alt="13-sp-2.png" width="907" height="535" class="jop-noMdConv">

### Step 3: install the necessary applications.

> There are other necessary applications should be installed on AIO-13 after the apps mentioned in **Step 3** of [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).
> 
> 3.1 Install [Windows Management Framework 5.1](https://www.microsoft.com/en-us/download/details.aspx?id=54616).
> <img src="https://s2.loli.net/2022/09/15/eZjuBUIlxJGRF1m.png" alt="aio13-3.4.1.png" width="828" height="488" class="jop-noMdConv">
> 
> > 3.1.1 Select "Win8.1AndW2K12R2-KB3191564-x64.msu" and click Next.
> > <img src="https://s2.loli.net/2022/09/15/eUxbYF2n4DO89dt.png" alt="aio13-3.4.2.png" width="806" height="457" class="jop-noMdConv">
> > 
> > 3.1.2 Click on "I Accept" button in the pop-up.
> > <img src="https://s2.loli.net/2022/09/15/oZ2UDzpAVEN6yu3.png" alt="aio13-3.4.2.png" width="643" height="451" class="jop-noMdConv"> 
> > <br>
> > 3.1.3 Click on **Restart Now** button. <br>
> > <img src="https://s2.loli.net/2022/09/15/O1uI2QoyPgW8FRN.png" alt="aio13-3.4.3.png" width="645" height="454" class="jop-noMdConv">
> 
> 3.2 Install [Microsoft Filter Pack 2.0](https://www.microsoft.com/en-us/download/details.aspx?id=17062).
> 
> > 3.2.1 Click on **Download** button.
> > <img src="https://s2.loli.net/2022/09/15/62w5KSqIzJ3la7R.png" alt="aio13-3.6.1.png" width="905" height="516" class="jop-noMdConv">
> > 
> > 3.2.2 Select **filterpack64bit.exe** and click on **Next**.
> > <img src="https://s2.loli.net/2022/09/15/4WKkLfwFgeCNsGt.png" alt="aio13-3.6.2.png" width="903" height="454" class="jop-noMdConv">
> > 
> > 3.2.3 Double-click on the exe and click on **Next** in the pop-up.
> > <img src="https://s2.loli.net/2022/09/15/rHfiMOKhFgZUPv3.png" alt="aio13-3.6.3.png" width="622" height="506" class="jop-noMdConv">
> > 
> > 3.2.4 Click on **Next**. <br>
> > <img src="https://s2.loli.net/2022/09/15/WSBkQXnhFKao2vT.png" alt="aio13-3.6.4.png" width="627" height="543" class="jop-noMdConv"> <br>
> > 3.2.5 Click on **Ok**. <br>
> > ![aio13-3.6.5.png](https://s2.loli.net/2022/09/15/hOZF7RMDJPWHErm.png) <br>
> 
> 3.3 Install [Cumulative Update 23 for Exchange Server 2013 (KB4489622)](https://www.microsoft.com/en-us/download/details.aspx?id=58392).
> 
> > 3.3.1 click on **Download** button.
> > <img src="https://s2.loli.net/2022/09/15/iBdsjTpolkyg21r.png" alt="aio13-3.7.1.png" width="896" height="529" class="jop-noMdConv">
> > 
> > 3.3.2 Double-click on the ISO and in the pop-up, click on **OK**. You can change the folder path of ISO later, for example, move them to the path "C:\\EX". 
> > <br>
> > ![aio13-3.7.2.png](https://s2.loli.net/2022/09/15/JMVd5sL8gnFeabu.png) 
> > <br>
> > 3.3.3 Wait for extracting. 
> > <br>
> > ![aio13-3.7.3.png](https://s2.loli.net/2022/09/15/tmdbBzpYOjEfAu8.png)
> > <br>
> > The installation of necessary apps is complete.
> > 
> > <br>
> > When you install [Unified Communications Managed API 4.0 Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=34992) on AIO-13, you may meet the following problem.
> > <br>
> >
> > **Problem**: If you met the pop-up lick the below pic, you can follow the solution with this link: <br>[Microsoft Communications Managed API 4.0 Install Error | PeteNetLive](https://www.petenetlive.com/KB/Article/0000746) 
> > <br>
> > ![aio13-if-3.1.png](https://s2.loli.net/2022/09/15/IBD9NZJuKvPHxse.png)
> > 
> > **Solution**: <br>
> > Run the cmdlet and then restart the system: 
> > ```
> > Install-WindowsFeature Server-Media-Foundation
> > ```
> > <img src="https://s2.loli.net/2022/09/15/Mojrt8VxZn6FDQC.png" alt="aio13-if-3.2.png" width="876" height="641" class="jop-noMdConv">

### Step 4: pending the ISO.

Same as **Step 4** in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).

### Step 5: prepare Windows Features.

> 5.1 Install the RSAT Feature.
> 
> ```
> Install-WindowsFeature RSAT-ADDS
> ```
> 
> 5.2 Install Exchange roles.
> 
> ```
> Install-WindowsFeature AS-HTTP-Activation, Desktop-Experience, NET-Framework-45-Features, RPC-over-HTTP-proxy, RSAT-Clustering, RSAT-Clustering-CmdInterface, RSAT-Clustering-Mgmt, RSAT-Clustering-PowerShell, Web-Mgmt-Console, WAS-Process-Model, Web-Asp-Net45, Web-Basic-Auth, Web-Client-Auth, Web-Digest-Auth, Web-Dir-Browsing, Web-Dyn-Compression, Web-Http-Errors, Web-Http-Logging, Web-Http-Redirect, Web-Http-Tracing, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Lgcy-Mgmt-Console, Web-Metabase, Web-Mgmt-Console, Web-Mgmt-Service, Web-Net-Ext45, Web-Request-Monitor, Web-Server, Web-Stat-Compression, Web-Static-Content, Web-Windows-Auth, Web-WMI, Windows-Identity-Foundation
> ```
> 
> 5.3. Restart the system.

### Step 6: use wizard to install exchange server 2013.

> 6.1. Click on "setup" in the path of CU.
> <img src="https://s2.loli.net/2022/09/15/PvL3ED2G5xQd1ne.png" alt="aio13-5.1.png" width="850" height="482" class="jop-noMdConv">
> 
> 6.2. Click on "Don’t check for updates right now" and click on next. Then take the following steps as the pics display. <br>
> > <img src="https://s2.loli.net/2022/09/15/sdJDbeijW2nM1lx.png" alt="aio13-5.2.1.png" width="803" height="704" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/15/yR7aIi18PdgwHez.png" alt="aio13-5.2.2.png" width="705" height="616" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/3X4CPOUeB1sd79b.png" alt="aio13-5.2.3.png" width="695" height="601" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/oUnmRlPseNdOtpA.png" alt="aio13-5.2.4.png" width="692" height="601" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/2yDbpeVYEvarxST.png" alt="aio13-5.2.5.png" width="694" height="615" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/mXdgRTKybCIM1VO.png" alt="aio13-5.2.6.png" width="693" height="606" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/lIWEv1rLSh84qGQ.png" alt="aio13-5.2.7.png" width="720" height="638" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/GVDRkjSI1gLqMHW.png" alt="aio13-5.2.8.png" width="719" height="631" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/aK7wFhld8X61PA3.png" alt="aio13-5.2.9.png" width="717" height="630" class="jop-noMdConv"><img src="https://s2.loli.net/2022/09/15/Ppt8nRS3smGW1jA.png" alt="aio13-5.2.10.png" width="689" height="600" class="jop-noMdConv">
> 
> 6.3. Then wait for the installation. 
> <br>
> <img src="https://s2.loli.net/2022/09/15/9Yf3JSNrhDE7pls.png" alt="aio13-5.2.11.png" width="726" height="635" class="jop-noMdConv">
> <br>

### Step 7: install o365.
Same as **Step 8** in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).


### Preparation mentioned in Overview.
Same as **Preparation mentioned in Overview** in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md)