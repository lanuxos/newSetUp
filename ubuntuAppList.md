# ubuntu app list
# Terminal
- update && upgrade
```bash
sudo apt update && apt upgrade -y
```
- install synaptic
```bash
sudo apt install synaptic
```
- install media codecs
```bash
sudo apt install ubuntu-restricted-extras
sudo apt install ubuntu-restricted-addons
```
- install GNOME Tweak
```bash
sudo apt install gnome-tweaks
# if E: Unable to locate package gnome-tweaks
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo apt update
sudo apt install gnome-tweaks
```
- install GNOME shell extensions
```bash
sudo apt install gnome-shell-extensions
```
- enable minimize on click
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```
- install GNOME sushi
```bash
sudo apt install gnome-sushi
```
- install ubuntu cleaner
```bash
sudo add-apt-repository ppa:gerardpuig/ppa
sudo apt-get update
sudo apt-get install ubuntu-cleaner
```
- install flatpak
```bash
sudo add-apt-repository ppa:alexlarsson/flatpak
sudo apt update
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
- install wine
```bash
sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ bionic main'
sudo apt-get install --install-recommends wine-stable
```
- install net-tools
```bash
sudo apt install net-tools
```
- install CPU-X
```bash
sudo apt install cpu-x
```
- install curl
```bash
sudo apt install curl
```
- install git
```bash
sudo apt install git
```
- install FSearch
```bash
sudo add-apt-repository ppa:christian-boxdoerfer/fsearch-stable
sudo apt update
sudo apt install fsearch
```

- install tailscale
```bash
curl -fsSL https://tailscale.com/install.sh | sh
```

- install nodejs
```bash
sudo apt install nodejs
```

- install docker
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
- clean system
```bash
sudo apt autoclean
sudo apt autoremove
```
# App Center [Snap]
- cpu-x
- Darktable
- firefox
- golang
- GIMP
- InkScape
- launchy
- LibreOffice
- Master PDF Editor
- OpenShot
- pgAdmin4
- postman
- sqlitebrowser
- sublimetext3
- transmission
- vlc
- vscode

# .deb
- [anydesk](https://anydesk.com/en/downloads/linux#linux-downloads)
- [docker](https://desktop.docker.com/linux/main/amd64/docker-desktop-amd64.deb?utm_source=docker&utm_medium=webreferral&utm_campaign=docs-driven-download-linux-amd64)
- [Google Chrome](https://www.google.com/chrome/)
- [filezilla](https://dl4.cdn.filezilla-project.org/client/FileZilla_3.67.1_x86_64-linux-gnu.tar.xz?h=MpxUROlEq0OveKEpiSqIJw&x=1728384983)
- [FreeFileSync](https://freefilesync.org/download/FreeFileSync_13.7_Linux.tar.gz)
- [teamviewer](https://dl.teamviewer.com/download/linux/version_15x/teamviewer_15.58.4_amd64.deb?ref=https%3A%2F%2Fwww.teamviewer.com%2Fen%2Fdownload%2Flinux%2F)
- [virtualbox](https://download.virtualbox.org/virtualbox/7.1.2/virtualbox-7.1_7.1.2-164945~Ubuntu~noble_amd64.deb)

# Gnome Extensions
- GSConnect
- Clipboard Indicator
- Coverflow Alt-Tab
- Shutdown Timer
- Transparent Top Bar

# Flatpak