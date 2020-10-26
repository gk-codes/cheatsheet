# CMD

Start a new PowerShell instance with `ExecutionPolicy` set to `Bypass`:

```text
powershell.exe -exec bypass
```

Compare 2 folders and log the differences \(nothing gets copied\):

```text
robocopy D:\SOURCE_DIR E:\TARGET_DIR /L /TS /MIR /LOG:D:\diff.txt
```

Mirror a directory:

```text
robocopy SOURCE DESTINATION /MIR /MT
```

`/MT` - Multi Threaded

