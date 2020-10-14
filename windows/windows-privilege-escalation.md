# Windows Privilege Escalation

### Tools

#### winPEAS

{% embed url="https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS" %}

For color-coded output, add a registry key and reopen the command prompt:

```text
reg add HKCU\Console /v VirtualTerminalLevel /t REG_DWORD /d 1
```

Example commands:

```text
.\winPEASany.exe quiet cmd fast
.\winPEASany.exe quiet cmd systeminfo
```

#### accesschk.exe

TODO

#### Seatbelt

Code: [https://github.com/GhostPack/Seatbelt](https://github.com/GhostPack/Seatbelt)

Pre-Compiled: [https://github.com/r3motecontrol/Ghostpack-CompiledBinaries/blob/master/Seatbelt.exe](https://github.com/r3motecontrol/Ghostpack-CompiledBinaries/blob/master/Seatbelt.exe)

#### PowerUp

 [https://raw.githubusercontent.com/PowerShellEmpire/PowerTools/master/PowerUp/PowerUp.ps1](https://raw.githubusercontent.com/PowerShellEmpire/PowerTools/master/PowerUp/PowerUp.ps1)

Dot source to load the script in a PowerShell prompt:

```text
. .\PowerUp.ps1
```

Check for common privilege escalation misconfigurations:

```text
Invoke-AllChecks
```

#### SharpUp

Run [SharpUp](https://github.com/GhostPack/SharpUp) in a cmd prompt:

```text
.\SharpUp.exe
```

Pre-Compiled SharpUp: [https://github.com/r3motecontrol/Ghostpack-CompiledBinaries/blob/master/SharpUp.exe](https://github.com/r3motecontrol/Ghostpack-CompiledBinaries/blob/master/SharpUp.exe)

PsExec tool from Windows Sysinternals: [https://docs.microsoft.com/en-us/sysinternals/downloads/psexec](https://docs.microsoft.com/en-us/sysinternals/downloads/psexec)

### When RDP is available

Add low privileged user to the administrators group:

```text
> net localgroup administrators <username> /add
```

