# AIO-19 LAB SETUP

## Overview


**References:**

- [Exchange Server prerequisites](https://learn.microsoft.com/en-us/exchange/plan-and-deploy/prerequisites?view=exchserver-2019)
- [Exchange Server system requirements](https://learn.microsoft.com/en-us/exchange/plan-and-deploy/system-requirements?view=exchserver-2019)
- [Use unattended mode in Exchange Setup](https://learn.microsoft.com/en-us/exchange/plan-and-deploy/deploy-new-installations/unattended-installs?view=exchserver-2019#use-setupexe-to-install-exchange-in-unattended-mode)
- [Step by Step Installation of Exchange Server 2019](https://xpertstec.com/step-by-step-installation-of-exchange-server-2019/)


| **EX19_AIO** |     |     |
| --- | --- | --- |
| Host | shgbsvmas | [VMAS - Workspaces](https://shgbsvmas/#/Workspaces) |
| Host Name | AIO-19 |     |
| Role | DC & MBX & Outlook |     |
| OS Version | Windows Server 2019 Datacenter (GA) Desktop|     |
| Original OS Language | English (en-us) |     |
| Additional Language Packs | Simplified Chinese (zh-cn)<br>Traditional Chinese (zh-tw) |     |
| Exchange Build Number | CU12 | Exchange Server build numbers and release dates<br>[https://docs.microsoft.com/en-us/exchange/new-features/build-numbers-and-release-dates?view=exchserver-2019](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fexchange%2Fnew-features%2Fbuild-numbers-and-release-dates%3Fview%3Dexchserver-2019&data=05%7C01%7Ct-fsheng%40microsoft.com%7C782fa10a65eb4f329d1508da8bfb2e12%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637976208194977653%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=KP6Ut9En9lE7r7O5K4WpgyqFWTr%2BTZlC7kEsCGCW3E8%3D&reserved=0) |
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


Here are the deferences of deployment between the AIO-19 and the general AIO. For more information about the general deployment of AIO, see [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).

### Step 1: configure the all-in-one virtual machine on VMAs.

>1.3. In the pop up **New Workspace**, type "2019" in the Filter Operating Systems, add one **Windows 2019 Datacenter (GA) Desktop**, and click on **Next** at the **Step 1** tab.
>![Screenshot _519_.png](https://s2.loli.net/2022/09/20/g1kzrKlSdh5oEwX.png)


### Step 2: login the AIO with RDCMan.exe.

Refer to the 'Step 2' in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).


### Step 3: install necessary applications.

You need to install apps below: 
1. Microsoft Edge Browser.
2. .NET Framework 4.8.
3. Visual C++ Redistributable Package for Visual Studio 2013
4. Unified Communications Managed API 4.0 Runtime
5. IIS URL Rewrite 2.1
6. Cumulative Update 12 for Exchange Server 2019

The installation of 1~4 refer to 'Step 3' of [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md);

The installation of 5 refer to 'Step 3' of [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md);

The installlation of 6 refer to the below: 
Please download [Cumulative Update 12 for Exchange Server 2019 (KB5011156)](https://www.microsoft.com/en-us/download/details.aspx?id=104131).
![3.png](https://s2.loli.net/2022/09/20/drYbXj9mp5TyBRe.png)


### Step 4: pending the ISO.
Refer to 'Step 4' of [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).

### Step 5: install Windows Features.
Refer to 'Step 5' of [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).

### Step 6: prepare AD schema, AD, and domain.
Refer to 'Step 6' of [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).

### Step 7: install exchange mailbox role
Refer to 'Step 7' of [AIO-16 LAB SETUP](AIO-16%20LAB%20SETUP.md).

### Step 8: install o365.
Same as **Step 7** in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).

### Preparation mentioned in Overview.
Same as **Preparation mentioned in Overview** in [General Deployment of AIO Step by step](General%20Deployment%20of%20AIO%20Step%20by%20step.md).