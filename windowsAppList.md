[# choco administrative powershell install script](https://chocolatey.org/install)
```powershell
Set-ExecutionPolicy AllSigned
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
# choco basic packages
```powershell
choco install revo-uninstaller 7zip.install firefox foobar2000 googlechrome sumatrapdf.install teamviewer vlc wechat whatsapp winrar -y
```

```powershell
choco install cpu-z.install crystaldiskinfo curl docker-desktop everything ffmpeg filezilla git-fork git.install golang googledrive greenshot io-unlocker kdeconnect-kde k-litecodecpackfull launchy lockhunter microsoft-windows-terminal nodejs.install notepadplusplus ntop.portable onedrive pgAdmin4 postman powertoys putty.install python qbittorent rufus sqlitebrowser sublimetext3 tailscale telegram teracopy virtualbox visualstudio2022community vscode windirstat wsl -y
```

# choco alternative basic packages
```powershell
choco install airdroid -y
choco install allway-sync -y
choco install anydesk.install -y
choco install ditto -y
choco install gimp -y
choco install innosetup -y
choco install itunes -y
choco install keepassxc -y
choco install mousewithoutborders -y
choco install nmap -y
choco install openvpn -y
choco install procexp -y
choco install procman -y
choco install rambox
choco install thonny -y
choco install tor-browser -y
choco install unifiedremote -y
choco install wireshark -y
choco install youtube-dl -y
```

# other source
microsoft office suit
adobe photoshop
adobe illustrator
adobe ligthroom
cisco packet tracer
ultraISO

foxit pdf
FreeFileSync
lao script

# [Win11Debloat](https://github.com/Raphire/Win11Debloat.git)
```powershell
& ([scriptblock]::Create((irm "https://win11debloat.raphi.re/"))) -RunDefaults -Silent
```

# [winutil](https://github.com/ChrisTitusTech/winutil)
```powershell
irm "https://christitus.com/win" | iex
```
