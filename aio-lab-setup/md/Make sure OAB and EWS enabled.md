# Make sure OAB and EWS enabled

## Make sure OAB enabled
### Step 1: verify the offline address book.
```
Get-OfflineAddressBook
```
![oab-get.png](https://s2.loli.net/2022/09/16/rsGhIMxfQCql3ek.png)

### If you want to configure OAB, take the following steps.
### Step 2: select a user mailbox and configure its OU.
> 2.1 Go to **EAC --> recipients --> mailboxes**.
>> 2.1.1 Double-click on a user mailbox**(for example, user1).
>> ![oab-2.1.1.png](https://s2.loli.net/2022/09/16/4h9d2byuVzxGvBj.png)
>> 
>> 2.1.2 Click on **More Options**.
>> ![oab-2.1.2.png](https://s2.loli.net/2022/09/16/s12aWMvzTyGRUSc.png)
>> 
>> 2.1.3 Click on **Edit** icon.
>> ![oab-2.1.3png.png](https://s2.loli.net/2022/09/16/A4I8tJZdDS3i2Cj.png)
>> 
>> 2.1.4 Print in "OU_Test" and click on **Ok**, then click on **Save**.
>> ![oab-2.1.4.1.png](https://s2.loli.net/2022/09/16/SjftTKUsoqdv5Vk.png)
>> 
>> ![oab-2.1.4.2.png](https://s2.loli.net/2022/09/16/MBH95Yh8t1mGDEs.png)
>
> 2.2 Run **EMS (Exchange Management Shell)** as admin.
>> 
>> 2.2.1 View the default offline address book.
>> ```
>> Get-OfflineAddressBook
>> ```
>> ![oab-get.png](https://s2.loli.net/2022/09/16/rsGhIMxfQCql3ek.png)
>> 
>> 2.2.2 Find mail server host.
>> ```
>>Get-Mailbox -Arbitration | where {$_.PersistedCapabilities -like "*oab*"}_
>> ```
>> ![oab-2.2.2.png](https://s2.loli.net/2022/09/16/poNtkVHL5fd4euc.png)
>> 
>> 2.2.3 View address lists.
>> ```
>>Get-AddressList
>> ```
>> ![oab-2.2.3.png](https://s2.loli.net/2022/09/16/yrxQGlKX7Oo4he1.png)
>> 
>> 2.2.4 Create an offline address book named Test, "All contacts" maybe replaced by address list you create.
>> ```
>>New-OfflineAddressBook -Name Test -AddressLists "All contacts" -VirtualDirectories "<server alias\>\OAB (Default Web Site)"
>>```
>> ![oab-2.2.4.png](https://s2.loli.net/2022/09/16/aXsI75qFMDwCeLN.png)
>> 
>> 2.2.5 Assign offline address book to recipients.
>> ```
>>Get-Mailbox -Filter {CustomAttribute1 -eq "OU_Test"} | Set-Mailbox -OfflineAddressBook "<alias\>"
>> ```
>> 
>> 2.2.6 Update the changes manually.
>> ```
>>Update-OfflineAddressBook "Test"
>> ```
>> ![oab-2.2.6.png](https://s2.loli.net/2022/09/16/EscH3o1TtRl8xPy.png)

## Make sure OAB enabled

### Step 1: verify the excahnge web services.
```
Get-WebServicesVirtualDirectory |Select name, *url* | fl
```
