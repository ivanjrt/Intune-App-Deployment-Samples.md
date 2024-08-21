Intune Apps AdobeReaderDC

Download the following:
https://get.adobe.com/reader/enterprise/
https://www.adobe.com/devnet-docs/acrobatetk/tools/Wizard/index.html
https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool/archive/refs/heads/master.zip
A png , jpeg logo for the app

# Step 1: Creating Raw Binaries
Extract the Adobe Executable within an isolated folder (As this will All get compressed for the App itself) <br/>
Install the Wizard File as this will help to create the Deployment binaries <br/>

Open the Wizard and select the MSI extracted file then choose: <br/>
![image](https://github.com/user-attachments/assets/f13f681e-2914-4346-ac41-e78e8cef2924) <br/>
![image](https://github.com/user-attachments/assets/96c57236-2986-4db6-b91c-2a8b8444c823) <br/>
![image](https://github.com/user-attachments/assets/7c385c83-4a45-423c-87dd-1586577ff1cb) <br/>
![image](https://github.com/user-attachments/assets/e31ac53f-6ecb-430e-898e-218f85737ff6) <br/> <br/>
it would look something like: (our config is the MST file) <br/>
![image](https://github.com/user-attachments/assets/a06deb7f-578f-4ec7-9a72-002bcaa3d9e5) <br/>

Try to install/Uninstall it locally first. (give it about 5 and 5 mins)
from the command line:
```java
setup.exe -s /msi /L*v "%programdata%\Intune-AdobeReaderDC-Install.log"
```
it will also generate a log in the programdata , within you will find the ProductCode
To Uninstall:
```java
Msiexec.exe /X {AC76BA86-7AD7-1033-7B44-AC0F074E4100} /qn /norestart /L*v "%programdata%\Intune-AdobeReaderDC-Uninstall.log"
```
**TIP:** Another way to find the product code:
``` Get-WmiObject -Class Win32_Product | Where-Object {$_.name -like "Adobe*"} ```

# Step 2: Converting Intune Binaries
![image](https://github.com/user-attachments/assets/d27386c5-20f7-495c-b88e-b6e1737bb9ab)

# Step 3: Intune Upload
Apps > All Apps > +Add > <br/>
And because we created an IntuneWim App, pick WIN32 <br/>
![image](https://github.com/user-attachments/assets/50248b18-fe7c-480e-89d5-9dd062476767) <br/>
Point at the file, you have uploaded <br/>
![image](https://github.com/user-attachments/assets/5cfbf317-a291-47e1-ba7c-f50214dfd9b5) <br/>
because we chosen the MSI file some of the fields will be automatically loaded however might not be accurate. IE: the version <br/>
the Program info also we can leave as is but for the sake of the purpose we change it to,
![image](https://github.com/user-attachments/assets/69343c54-97d4-4f36-8436-91091b46fcfb)
![image](https://github.com/user-attachments/assets/4af0b28f-f93a-4355-b49a-fa73f1ab1444)
![image](https://github.com/user-attachments/assets/29e79a33-808f-4104-85f6-16c6a458bfaa)
![image](https://github.com/user-attachments/assets/ae1ad65d-c013-4cba-97a2-ff1f075ecb12)
![image](https://github.com/user-attachments/assets/5fffaee9-3f8b-4a1b-a5ce-83b8871e374f)
![image](https://github.com/user-attachments/assets/615147e4-138e-466c-bdab-546e3f64259a)
![image](https://github.com/user-attachments/assets/715dc5f3-fb1d-473e-928d-63d12e956221)
![image](https://github.com/user-attachments/assets/02816f58-4497-4257-8e09-900b294164e4)




