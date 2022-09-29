# Enable ActiveSync device connectivity

### Step 1. Check ActiveSync device connectivity: 
	
```
Get-ActiveSyncDevice -Mailbox "contoso/<mailbox name>"
```

### Step 2. Enable EMS with cmdlet: 
	
```
Set-CasMailbox -Identity "user1" -ActiveSyncEnabled $true
```