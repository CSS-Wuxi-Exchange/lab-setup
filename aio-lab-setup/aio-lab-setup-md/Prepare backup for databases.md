# Prepare backup for databases

## Prerequisities: 
Prepare addtional disk for Backup issue. you can see more details from [Prepare additional disk for Backup issue.](../Fangyuan%20@%20Microsoft/Prepare%20additional%20disk%20for%20Backup%20issue.md).

## Step by Step:
### Step 1.

Login the server and go to 'Windows Server Backup'.

> Follow the below actions: **Server Manager --> Tools --> 'Windows Server Backup'**
> 
> If 'Windows Server Backup' displays like the below pic, you need to install it with EMS.
> <img src="https://s2.loli.net/2022/09/19/pRn7xl6DMH2hVyP.png" alt="b-1.1.png" width="743" height="469" class="jop-noMdConv">
> 
> ```
> Install-WindowsFeature Windows-Server-Backup
> ```
> 
> <img src="https://s2.loli.net/2022/09/19/scilZTIECwqXef3.png" alt="b-1.2.png" width="744" height="389" class="jop-noMdConv">
> 
> Successfully installed.

### Step 2.

Enter 'Windows Server Backup'.

> 2.1 Follow the below actions: **Server Manager --> Tools --> 'Windows Server Backup'**.
> 
> 2.2 Click on 'Backup Once'.
> <img src="https://s2.loli.net/2022/09/19/xf8nsR4mOqvCj1J.png" alt="b-2.png" width="735" height="489" class="jop-noMdConv">

### Step 3.

Configure backup with Wizard.

> 3.1 In 'Backup options', select 'Different options'. Then click on 'Next'.
> <img src="https://s2.loli.net/2022/09/19/J4c2wGOFdHxmv8l.png" alt="Screenshot 508.png" width="705" height="586">
> 
> 3.2 In 'Select Backup Configuration', select 'Custom'.
> ![Screenshot 509.png](https://s2.loli.net/2022/09/19/AeWFwDvNzL7VUuj.png)
> 
> 3.3 In 'Select Items for Backup', click on 'Add items' button.
> ![Screenshot 510.png](https://s2.loli.net/2022/09/19/Rywbk3zOFZHY6jv.png)
> 
> Then click on folders following the location of the database that you want to backup. (In this scenario, the location of database on AIO-13 is 'c:\\program files\\microsoft\\exchange servers\\v15\\mailbox&lt;database name&gt;')
> ![Screenshot 511.png](https://s2.loli.net/2022/09/19/3u91sWNacmKpFeg.png)
> 3.4 In 'Select Items for Backup', click on 'Advanced items' button.
> ![Screenshot _512_.png](https://s2.loli.net/2022/09/19/QhAdRxrwnUS1uEP.png)
> 
>> 3.4.1 Navigate to 'VSS Settings', click on 'VSS full Backup', click on 'OK'.
>> ![Screenshot _513_.png](https://s2.loli.net/2022/09/19/OJ5xu6hAK2jS1qG.png)
>> 3.4.2 Then click on 'Next'.
>> ![Screenshot _514_.png](https://s2.loli.net/2022/09/19/Vtgsc7b4lG8UaWQ.png)
> 
> 3.5 In 'Specify Destination Type', select 'local drives'.
> ![Screenshot _515_.png](https://s2.loli.net/2022/09/19/OPWHlrfAQzKINdb.png)
> 
> Then click on 'Next'.
> ![Screenshot _512_.png](https://s2.loli.net/2022/09/19/QhAdRxrwnUS1uEP.png)
> 
> 3.6 In 'Configuration', click on 'Backup'. 
> ![Screenshot _517_.png](https://s2.loli.net/2022/09/19/7N62yvXjUdSTqni.png)
> 
> 3.7 In 'Backup Progress', when the status is completed, click on 'Close'.
> ![Screenshot _518_.png](https://s2.loli.net/2022/09/19/vyVqY2KBTCF6caO.png)