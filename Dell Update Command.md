# Dell Update Command.

Download it from here: https://www.dell.com/support/kbdoc/en-us/000177325/dell-command-update <br/>
Install command line: <br/>

# Install command line:
```java
Dell-Command-Update-Application-for-Windows-10_GRVPK_WIN_4.3.0_A00_03Dell-Command-Update-Application-for-Windows-10_GRVPK_WIN_4.3.0_A00_03.exe /s /l=C:\ProgramData\Intune-DellUpdate-Install.txt
```

# Uninstall: (comfirm App GUID)
```java
msiexec /x {5669AB71-1302-4412-8DA1-CB69CD7B7324} /qmsiexec /x {5669AB71-1302-4412-8DA1-CB69CD7B7324} /q
```

# Detection
```java
File C:\Program Files\Dell\CommandUpdate\readme.txt
```


