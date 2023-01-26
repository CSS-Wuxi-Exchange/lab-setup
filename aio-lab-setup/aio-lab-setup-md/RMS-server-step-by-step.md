# install RMS server step by step and integrate with exchange server
## ADRMS
1.	Install AD RMS role and related management tool
Install-WindowsFeature ADRMS -IncludeManagementTools
>>![image.png](https://s2.loli.net/2023/01/20/uIO3derSRyxN8Xi.png)
2.	Launch server manager -> notification -> perform additional configuration
>>![image.png](https://s2.loli.net/2023/01/20/UWmvMK5Y3hI9eEg.png)
3.	Choose "create a new AD RMS root cluster")
>>![image.png](https://s2.loli.net/2023/01/20/5petuO61J4Ssgyn.png)
4.	Choose "use windows internal database on this server" since we don't have SQL server database here
>>![image.png](https://s2.loli.net/2023/01/20/bK9QBsF7wOtNuXa.png)
5.	Specify a service account
>>![image.png](https://s2.loli.net/2023/01/20/VyEWDOZs7XQFimH.png)
6.	Select Cryptographic mode 2
>>![image.png](https://s2.loli.net/2023/01/20/r3Oo5AfQH2YF8E9.png)
7.	Select "use AD RMS centrally managed key storage" here
>>![image.png](https://s2.loli.net/2023/01/20/XPJZlch4nkMRaIr.png)
8.	Select the web site
>>![image.png](https://s2.loli.net/2023/01/20/c7DaIFngEJ65ko2.png)
9.	Enter the address
>>![image.png](https://s2.loli.net/2023/01/20/ZGSmOyAgPL5YNMX.png)
10.	Select the certificate
>>![image.png](https://s2.loli.net/2023/01/20/SiIRZJKCUaBGWMQ.png)
11.	Register SCP now
>>![image.png](https://s2.loli.net/2023/01/20/jJzpyVBUiFReD91.png)
12.	Install the RMS service
>>![image.png](https://s2.loli.net/2023/01/20/VdmIiDgZ8ahYLSp.png)
13.	Confirm exchange servers group and  AD RMS service group have read/read&execute permission on servercertificateion.asmx, publish.asmx
>>![image.png](https://s2.loli.net/2023/01/20/jlUROxbFiZ3Ak1y.png)
>>![image.png](https://s2.loli.net/2023/01/20/7q5IVT9dU1HQKk3.png)
14.	Log off rms server and log on again.
15.	Create a RMS super user group, and add FederatedEmail.4c1f4d8b-8179-4148-93bf-00a95fa1e042 to the group
>>![image.png](https://s2.loli.net/2023/01/20/HhxeCMaFK9Uusv1.png)
16.	Open active directory rights management service -> security policies -> super user -> enable super users -> change super user group -> choose the rms super user group
>>![image.png](https://s2.loli.net/2023/01/20/xdBGEqSJPseCRbM.png)
17.	Set-IRMConfiguration -InternalLicensingEnabled $true and reset IIS
>>![image.png](https://s2.loli.net/2023/01/20/5KSLn9XYi8UgGDE.png)
18.	Test-irmconfiguration, confirming the result is pass
>>![image.png](https://s2.loli.net/2023/01/20/ZdPoThRUXeqiNJL.png)
Also, the encrypted message can be successfully opened in outlook
>>![image.png](https://s2.loli.net/2023/01/20/zp5tvRqSNiVJlKb.png)