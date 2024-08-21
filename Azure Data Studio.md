Download the following:
https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15 (System Installer Version) <br/>

# Step 1: Configuring the Binaries
Put this file in a isolated folder, and test it first <br/>

Installation command. example: <br/>
```
azuredatastudio-windows-setup-1.32.0.exe /VERYSILENT /MERGETASKS=!runcode /LOG="%programdata%\Intune-AZDataStudio-Install.log"
```
Uninstall command. example: <br/>
```
"C:\Program Files\Azure Data Studio\unins000.exe" /LOG="%programdata%\Intune-AZDataStudio-Uninstall.log" /VERYSILENT
```
File Detection: <br/>
```
C:\Program Files\Azure Data Studio\azuredatastudio.exe
```

# Step 2: Converting Intune Binaries
In the Intune Zip file we only need the intuneWinAppUtil, on a separate folder, and an destination folder for the intune Binary then launch it in the command line <br/>
![image](https://github.com/user-attachments/assets/0a0b2a20-ce48-407a-bbf6-cd63e1855ca2) <br/>


# Step 3: Intune Upload
![image](https://github.com/user-attachments/assets/6bf6492d-84a7-4344-9936-c6f8bd35f822) <br/>
![image](https://github.com/user-attachments/assets/388e456a-73d2-48f4-913d-d5c121c77a20) <br/>
![image](https://github.com/user-attachments/assets/be5a6882-a89c-4f41-8305-b811129180be) <br/>
For requirement Rules you can add Registries, Files, or scrtips <br/>
![image](https://github.com/user-attachments/assets/17149354-6b53-46cf-a6f8-e200e5f43c3f) <br/>
![image](https://github.com/user-attachments/assets/810d5d3f-e9b7-4fc0-97ce-52cab24b95be) <br/>
![image](https://github.com/user-attachments/assets/0b28269a-8336-4a2c-8ca4-7f5c0ad4e8a1) <br/>
![image](https://github.com/user-attachments/assets/8f85c0f8-6f0a-4e27-88bf-85c1fc20dffe) <br/>
![image](https://github.com/user-attachments/assets/083c98fd-cbc8-49a3-aa47-e3fa6ed0a30e) <br/>
