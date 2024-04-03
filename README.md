# useful

## Disable wsl terminal sound
add to `~/.bashrc`
```
# scheiss sound
bind 'set bell-style none'
```

## Disable bing search
in powershell
```powershell
REG ADD "HKCU\Software\Microsoft\Windows\CurrentVersion\Search" /V BingSearchEnabled /T REG_DWORD /D 0 /F
```
restart `explorer.exe`

## open vscode from wsl in current folder
create `code.bat` in `C:\Users\<USER>\AppData\Local\Microsoft\WindowsApps`
```bat
wsl.exe --cd %CD% code .
```
make sure that `code.bat` is found before the vscode `code` file in the PATH environment variable
