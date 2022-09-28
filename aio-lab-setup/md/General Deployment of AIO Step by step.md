# General Deployment of AIO Step by step

## Overview


| **AIO** | same or defer |     |     |
| --- | --- | --- | --- |
| Host | same | shgbsvmas | [VMAS - Workspaces](https://shgbsvmas/#/Workspaces) |
| Host Name | defer | AIO-13 or AIO-16 or AIO-19 |     |
| Role | defer | AIO-13 defers from AIO-16 & AIO-19 |     |
| OS Version | defer |     |     |
| Original OS Language | same | English (en-us) |     |
| Additional Language Packs | same | Simplified Chinese (zh-cn)<br>Traditional Chinese (zh-tw) |     |
| Exchange Build Number | defer |     | Exchange Server build numbers and release dates<br>[https://docs.microsoft.com/en-us/exchange/new-features/build-numbers-and-release-dates?view=exchserver-2019](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fexchange%2Fnew-features%2Fbuild-numbers-and-release-dates%3Fview%3Dexchserver-2019&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=KP6Ut9En9lE7r7O5K4WpgyqFWTr%2BTZlC7kEsCGCW3E8%3D&reserved=0) |
| Password Complexity | defer |     |     |
| Certificate created and configured | same | Exchange self-generated |     |
| Outlook Version | same | Microsoft 365 2019 |     |
| Outlook Language Packs | same | Simplified Chinese (zh-cn)<br>English (en-us)<br>Traditional Chinese (zh-tw) |     |
| Outlook Anywhere enabled | same | Y   |     |
| OAB and EWS enabled | same | Y   |     |
| Network Monitor installed | same | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Fiddler installed | same | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Telnet25 | same | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| ExTRA | same | Y   | [https://aka.ms/wxex](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Faka.ms%2Fwxex&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=6xq9Wi9gsCpPsToD6KFsM9Qhjp0bd5seqOoE4UmKbzg%3D&reserved=0) |
| Disable CRL check | same |     | Exchange 2010 Management Console (EMC) is very slow<br>[https://blogs.technet.microsoft.com/nawar/2011/06/03/exchange-2010-management-console-emc-is-very-slow/](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fblogs.technet.microsoft.com%2Fnawar%2F2011%2F06%2F03%2Fexchange-2010-management-console-emc-is-very-slow%2F&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=Hoo%2BgXCBkwvIWsFNDVQY9bxiem7vrN7qi8xtOVm8nvo%3D&reserved=0)<br>Configuring Exchange Servers Without Internet Access<br>[https://techcommunity.microsoft.com/t5/exchange-team-blog/configuring-exchange-servers-without-internet-access/ba-p/593692](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftechcommunity.microsoft.com%2Ft5%2Fexchange-team-blog%2Fconfiguring-exchange-servers-without-internet-access%2Fba-p%2F593692&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=%2BD6NVy2WMbhC%2FmJJ6Un5dwzDGw2gu1nEQ%2BnqjMLeXwY%3D&reserved=0) |
| NIC | same | Private IP |     |
| ActiveSync device connectivity | same | Y   |     |
| Additional disk for Backup issue | same | Y   |     |
| Enable Windows Server Backup | same | Y   |     |
| Backup | same | Y   |     |
| Snap Shot | same | Y   |     |
| Lab known issue | defer |     |     |
| FAQ |     |     |     |

* * *

## Deployment Step by step
<br>
(take the deployment of AIO-16 as example)

**References:**

- [Microsoft Exchange 2019 Beginners Video Tutorials Series](https://www.youtube.com/playlist?list=PLUZTRmXEpBy1HdGlhh3XSPD5WTAA_-wKN)

### Step 1: configure the all-in-one virtual machine on VMAs.

> 1.1. Log on [shgbsvmas - Workspaces](https://shgbsvmas/#/Workspaces).
> 
> 1.2. Click on **Workspaces** on the top toolbar and click on **New Custom Workspace.**
> <img src="https://s2.loli.net/2022/09/16/5Xk9BdfoyaqV3Yh.png" alt="aio-1.2.png" width="854" height="233" class="jop-noMdConv">
> 
> 1.3. In the pop up **New Workspace**, type \<version\>; in the **Filter Operating Systems**, select the OS system of AIO, and click Next at the **Step 1**. <br>
> <img src="https://s2.loli.net/2022/09/16/3Mq1nr8PNEh7j4R.png" alt="aio-1.3.png" width="754" height="555" class="jop-noMdConv">
> 
> 1.4. Click on **Private Network - Routable** and click on Next at the **Step 2**.
> <img src="https://s2.loli.net/2022/09/16/GShXHfubEJMyxvO.png" alt="aio-1.4.png" width="753" height="554" class="jop-noMdConv">
> 
> 1.5. Edit the name of your new workspace, and password. Then click on **Next** at the **Step 3** tab.
> <img src="https://s2.loli.net/2022/09/16/emRQunZUv7zygka.png" alt="aio-1.5.png" width="757" height="558" class="jop-noMdConv">
> 
> 1.6. Click on **Customize** at the **Done**!.
> 
> > <img src="https://s2.loli.net/2022/09/16/z4sIDh6lQGy3oeL.png" alt="aio-1.6.1.png" width="715" height="528" class="jop-noMdConv">
> > 
> > Now we can see one VM has been created.
> > <img src="https://s2.loli.net/2022/09/16/Uh1u5kH7boFT9yY.png" alt="aio-1.6.2.png" width="717" height="565" class="jop-noMdConv">
> 
> 1.7. Right-click on this virtual machine, and click on **Properties**.
> <img src="https://s2.loli.net/2022/09/16/IvApTsbOFjStgqr.png" alt="aio-1.7.png" width="740" height="633" class="jop-noMdConv">
> 
> 1.8. In the pop up **VM**, edit the **Virtual Machine Label, Computer Name** and click on the next tab **Hardware.**
> <img src="https://s2.loli.net/2022/09/16/CzEMjUm3iYvKR2l.png" alt="aio-1.8.png" width="740" height="783" class="jop-noMdConv">
> 
> 1.9. Select the processors as 8, the Min as 8 GB. Then click on the icon **Edit**, select the size as 300 GB, and click on **Save**.
> 
> > <img src="https://s2.loli.net/2022/09/16/fd7w68YzqHrJ4kK.png" alt="aio-1.9.1.png" width="858" height="585" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/16/BHdi7CW4YoqZPp5.png" alt="aio-1.9.2.png" width="848" height="583" class="jop-noMdConv">
> > 
> > When you finish these steps, you can the configuration of Hardware like the below pic, then click on the next tab **Domain**.
> > <img src="https://s2.loli.net/2022/09/16/wAOhf5b74educRV.png" alt="aio-1.9.3.png" width="693" height="470" class="jop-noMdConv">
> 
> 1.10. In the **Domain** tab, select **Domain Role** as Domain Controller, and edit **Domain Name** as contoso.com, then click on **Save Changes**.
> 
> > <img src="https://s2.loli.net/2022/09/16/J3FvdYrWbgCpDOR.png" alt="aio-1.10.1.png" width="698" height="465" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/16/l4yVcpmUnRrtgPq.png" alt="aio-1.10.2.png" width="687" height="692" class="jop-noMdConv">
> > 
> > When you finish these steps, you can see VMAs displays like the below pic.
> > ![aio-1.10.3.png](https://s2.loli.net/2022/09/16/nQTovYUjF2AwsqG.png)
> 
> 1.11. Click on the **Deploy** button at the bottom of the screen, and wait for deploying.
> 
> > <img src="https://s2.loli.net/2022/09/16/toI8UHsp6QDm1ha.png" alt="aio-1.11.1.png" width="643" height="344" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/16/PnNcQuMiAgJSh78.png" alt="aio-1.11.2.png" width="684" height="730" class="jop-noMdConv">
> 
> When the deployments on VMAs is finished, you can see the status of AIO is running.
> <img src="https://s2.loli.net/2022/09/16/SLd7mcH8iNPW1j4.png" alt="aio-1.11.3.png" width="671" height="584" class="jop-noMdConv">

### Step 2: login the AIO.

> 2.1. Click on **Connect** at the top toolbar, and click on **Download RDCMan File.**
> <img src="https://s2.loli.net/2022/09/16/7XMrkO68uveAJTS.png" alt="aio-2.1.png" width="657" height="594" class="jop-noMdConv">
> 
> 2.2. Open the file from RDCMan.exe.
> 
> > <img src="https://s2.loli.net/2022/09/16/hyk15IeU37vPCXl.png" alt="aio-2.2.1.png" width="783" height="441" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/16/DAOaZUFHxjElX5r.png" alt="aio-2.2.2.png" width="840" height="510" class="jop-noMdConv">
> 
> 2.3. Double-click on the &lt;server name&gt; and login.
> <img src="https://s2.loli.net/2022/09/16/8sM9JgRhKVTadvC.png" alt="aio-2.3.png" width="819" height="460" class="jop-noMdConv">

### Step 3: install necessary applications.

Apps need to be installed in all OS versions of AIOs are mentioned in this part:

- Microsoft Edge Browser
- .NET Framework 4.8
- Visual C++ Redistributable Package for Visual Studio 2013
- Unified Communications Managed API 4.0 Runtime

> 3.1. First install Edge Browser.
> 
> > 3.1.1 Copy **MicrosoftEdgeSetup.exe** from the on-premises machine.
> > <img src="https://s2.loli.net/2022/09/16/rAN48XxPeUtiBgy.png" alt="aio-3.1.1.png" width="821" height="484" class="jop-noMdConv">
> > 
> > 3.1.2 Paste it to the virtual machine, and install it.
> > <img src="https://s2.loli.net/2022/09/16/45QcirTesq1atMJ.png" alt="aio-3.1.2.png" width="761" height="390" class="jop-noMdConv">
> > 
> > 3.1.3 Don't forget to configure the default browser as Microsoft Edge. For more information, see [Change default apps](../Fangyuan%20@%20Microsoft/Change%20default%20apps.md).
> 
> 3.2. Open the edge and Install [.NET Framework 4.8](https://download.visualstudio.microsoft.com/download/pr/014120d7-d689-4305-befd-3cb711108212/0fd66638cde16859462a6243a4629a50/ndp48-x86-x64-allos-enu.exe).
> 
> > 3.2.1 Double-click, and select "I have…".
> > 
> > <img src="https://s2.loli.net/2022/09/15/g5oaFjwGtsCBZ6h.png" alt="aio-3.2.1.png" width="640" height="602" class="jop-noMdConv">
> > 
> > 3.2.2 In the pop-up, Click on "Yes".
> > 
> > <img src="https://s2.loli.net/2022/09/15/hW8zIQ74A9Cksut.png" alt="aio-3.2.2.png" width="642" height="605" class="jop-noMdConv">
> > 
> > 3.2.3 The installation of .Net Framework 4.8 is complete.
> > 
> > <img src="https://s2.loli.net/2022/09/15/NOmGfB6sjWby7oT.png" alt="aio-3.2.3.png" width="637" height="596" class="jop-noMdConv">
> > 
> > If you have already installed it, you will see this pop-up.
> > 
> > <img src="https://s2.loli.net/2022/09/15/XWFN6jOCraoi2yM.png" alt="13-sp-3-1.png" width="652" height="581" class="jop-noMdConv">
> 
> 3.3. Install [Visual C++ Redistributable Package for Visual Studio 2013](https://www.microsoft.com/en-us/download/details.aspx?id=40784).
> 
> <img src="https://s2.loli.net/2022/09/15/MGPVdUvofSp9sgn.png" alt="13-sp-3-3-1.png" width="767" height="454" class="jop-noMdConv">
> 
> > 3.3.1 Select **vcredist_x64.exe** and click on **Next**.
> > <img src="https://s2.loli.net/2022/09/15/fqUmZkzBCgo9wnQ.png" alt="13-sp-3-3-2.png" width="773" height="472" class="jop-noMdConv">
> > 
> > 3.3.2 Double-click on the exe and choose "I agree...", then install.
> > ![aio-3.3.2.png](https://s2.loli.net/2022/09/15/OAM7bPBLsrvmF9E.png)
> > 
> > 3.3.3 The installation of Visual C++ Redistributable Package for Visual Studio 2013 is complete.
> > ![aio-3.3.3.png](https://s2.loli.net/2022/09/15/fDMTGWxPlobOtLh.png)
> 
> 3.4 Install [Unified Communications Managed API 4.0 Runtime](https://www.microsoft.com/en-us/download/details.aspx?id=34992).
> 
> > 3.4.1 Click on **Download** button and wait for the process.
> > <img src="https://s2.loli.net/2022/09/15/kNYwitZDys6KpcA.png" alt="aio13-3.5.png" width="773" height="473" class="jop-noMdConv">
> > 
> > 3.4.2 Double-click on the **UcmaRuntimeSetup.exe** and in the pop-up, click on **Next**.
> > <img src="https://s2.loli.net/2022/09/15/5I7DvYmfCuxjr6h.png" alt="aio-3.5.2.png" width="645" height="612" class="jop-noMdConv">
> > 
> > 3.4.3 Select "I have read and accept…" and click on **Install**.
> > <img src="https://s2.loli.net/2022/09/15/ojnKCOlIdgGmBr8.png" alt="aio-3.5.3.png" width="650" height="609" class="jop-noMdConv">
> > 
> > 3.4.4 The installation of Unified Communications Managed API 4.0 Runtime is completed.
> > ![aio-3.5.4.png](https://s2.loli.net/2022/09/15/jdBN1ex5rkYoXtT.png)

After the above apps installed, there are other necessary apps should be installed on AIOs with different OS system.

- For more information of **AIO-13**'s necessary apps in the deployment, go to [AIO-13 LAB SETUP](AIO-13%20LAB%20SETUP.md).
    
- For more information of **AIO-16**'s necessary apps in the deployment, go to [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).
    
- For more information of **AIO-19**'s necessary apps in the deployment, go to [AIO-19 LAB SETUP](AIO-19%20LAB%20SETUP.md).

    

### Step 4: pending the ISO.

> Double-click on the &lt;Disk Image File&gt; and let the ISO stay pending.
> <img src="https://s2.loli.net/2022/09/16/eNnYBlU2a7xVvIq.png" alt="3.2.2.png" width="789" height="448" class="jop-noMdConv">
> 
> <img src="https://s2.loli.net/2022/09/16/RgDfIVM7QNHL1pE.png" alt="3.2.3.png" width="789" height="441" class="jop-noMdConv">

### When you finish the above steps, restart your system and reconnect. Do the following actions:

> - Restart the system: **WIN** icon --> **Power** --\> **Restart**.
> - Click on the AIO at the left side of console and click on **Reconnect server**.
>     <img src="https://s2.loli.net/2022/09/16/iTt7nahqIb2kBJg.png" alt="aio-reconnect.png" width="762" height="646" class="jop-noMdConv">

### Step 5: install windows features.

Details are different due to different OS system on AIO.

> For more information of **AIO-13**'s preparation, see **Step 5** in [AIO-13 LAB SETUP](AIO-13%20LAB%20SETUP.md).
> 
> For more information of **AIO-16**'s preparation, see **Step 5** in [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).
> 
> For more information of **AIO-19**'s preparation, see **Step 5** in [AIO-19 LAB SETUP](AIO-19%20LAB%20SETUP.md).

### Step 6: install exchange server.

Details are different due to different OS system on AIO. **This step is the same on AIO-13 and AIO-16**.

> For more information of **AIO-13**'s preparation, see **Step 6** in [AIO-13 LAB SETUP](AIO-13%20LAB%20SETUP.md).
> 
> For more information of **AIO-16**'s preparation, see **Step 6** & **Step 7** in [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).
> 
> For more information of **AIO-19**'s preparation, see **Step 6** & **Step 7** in [AIO-19 LAB SETUP](AIO-19%20LAB%20SETUP.md).

### Step 7: install o365.

> 7.1. Open [Office 365 Login | Microsoft Office](https://www.office.com/) with Edge and sign in as **&lt;alias&gt;@xxx.onmicrosoft.com**.
> <br>
> 7.2. Download o365 apps.<br>
> <img src="https://s2.loli.net/2022/09/16/rkV57n8Rbxeja29.png" alt="aio-7.2.png" width="723" height="806" class="jop-noMdConv">
> 
> 7.3. Install.
> 
> > <img src="https://s2.loli.net/2022/09/16/EIos5fhVHlWvUFn.png" alt="aio-7.3.1.png" width="681" height="640" class="jop-noMdConv"> <img src="https://s2.loli.net/2022/09/16/xlRvrwHDGA4g597.png" alt="aio-7.3.2.png" width="748" height="476" class="jop-noMdConv">
> 
> Then the **outlook** is installed.

### Preparation mentioned in Overview.

- Configure Language packs.
    \*\* See more details in [Configure Language packs](Configure%20Language%20packs.md)
- Make sure Outlook Anywhere enabled.
    \*\* See more details in [Make sure Outlook Anywhere enabled](Make%20sure%20Outlook%20Anywhere%20enabled.md)
- Make sure OAB and EWS enabled.
    \*\* See more details in [Make sure OAB and EWS enabled](Make%20sure%20OAB%20and%20EWS%20enabled.md)
- Install Network Monitor.
    \*\* See more details in [Install Network Monitor 3.4](Install%20Network%20Monitor%203.4.md)
- Install Fiddler.
    \*\* See more details in [Use Fiddler](Use%20Fiddler.md)
- Install Telnet25.
    \*\* See more details in [Install Telnet25](Install%20Telnet25.md)
- Install ExTRA.
    \*\* See more details in [Install ExTRA](Install%20ExTRA.md)
- Disable CRL check.
    \*\* See more details in [Disable CRL check](Disable%20CRL%20check.md)
- Make sure ActiveSync device connectivity enabled.
    \*\* See more details in [Enable ActiveSync device connectivity](Enable%20ActiveSync%20device%20connectivity.md)
- Prepare additional disk for Backup issue.
    \*\* See more details in [Prepare additional disk for Backup issue.](Prepare%20additional%20disk%20for%20Backup%20issue.md)
- Prepare backup for databases on AIO.
    \*\* See more details in [Prepare backup for databases](Prepare%20backup%20for%20databases.md)
- Create snap shots for AIO.
    \*\* See more details in [](Create%20snap%20shots.md)