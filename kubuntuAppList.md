# Kubuntu New Setup

# wifi not working
## probe with driver iwlwifi failed with error -110
```
lspci -nnk | grep -i network
dmesg | grep -i network
lsusb | grep -i intel
```

## note ID such as: 8087:0029
```
echo 'options usbcore.quirks=8087:0029:k' | sudo tee /etc/modprobe.d/usb-reset-quirk.conf
```

## update GRUB
```
sudo nano /etc/default/grub
```

## update line below
```
GUB_CMDLINE_LINUX_DEFAULT="quiet splash usbcore.quirk=8087:0029:k pcie_aspm=off"
```

## update GRUB
```
sudo update-grub
sudo reboot
```

## full cold boot the device
- turn of computer
- detach power/battery
- press and hold power button at least for 30 sec

# update
```
apt update
apt fullupgrade
apt autoclean
apt autoremove
```

# apt
```
apt install synaptic curl golang-go htop net-tools nodejs python3-pip python3-setuptools python3-venv thefuck transmission vlc

apt install darktable gimp inkscape libreoffice openshot-qt postgresql postgresql-contrib
```

# flatpak

```
# sudo add-apt-repository ppa:alexlarsson/flatpak
sudo apt install flatpak kde-config-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

flatpak install flathub com.anydesk.Anydesk org.chromium.Chromium net.code_industry.MasterPDFEditor org.mozilla.firefox org.videolan.VLC

flatpak install flathub org.filezillaproject.Filezilla com.getpostman.Postman org.pgadmin.pgadmin4 com.sublimetext.three tech.feliciano.pocket-casts org.sqlitebrowser.sqlitebrowser

flatpak run org.chromium.Chromium
```

# [code](https://code.visualstudio.com/docs/setup/linux)
```
sudo apt update
sudo apt install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" |sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
rm -f packages.microsoft.gpg
sudo apt install apt-transport-https
sudo apt install code
```

# zsh
```
apt install zsh -y
zsh
```
## change default shell to zsh [logout and re-login]
`chsh -s $(which zsh)`

## install oh-my-zsh
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

## plugins
```
conda
copybuffer
copyfile
copypath
dirhistory
dotenv
flutter
gcloud
git
golang
history
httpie
jira
jsontools
laravel
nmap
node
nvm
pep8
pip
python
ssh
sublime
sudo
thefuck
ufw
virtualenv
vscode
web-search
colored-man-pages
colorize
```

## zsh-autosuggestions
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

## zsh-syntax-highlighting
`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

## theme
### install fonts
- [MesloLGS NF Regular.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf)
- [MesloLGS NF Bold.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf)
- [MesloLGS NF Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf)
- [MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf)

### install theme
[powerlevel10k/powerlevel10k](https://github.com/romkatv/powerlevel10k)
`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"`

### update zsh theme [~/.zshrc]
`ZSH_THEME="powerlevel10k/powerlevel10k"`

### restart zsh
`exec zsh`

### config powerlevel10k theme
`p10k configure`

# [anaconda](https://www.anaconda.com/docs/getting-started/anaconda/install#linux)
```
curl -O https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh
bash ~/Anaconda3-2024.10-1-Linux-x86_64.sh
source ~/.zshrc
```

# [TeamViewer](https://download.teamviewer.com/download/linux/teamviewer_amd64.deb)
```
sudo apt install gdebi                  # sudo apt install libminizip1 gdebi-core
sudo apt install ./TEAMVIEWER...deb     # sudo gdebi-core ./TEAMVIEWER...deb
```

# grub-customizer
```
sudo add-apt-repository ppa:danielrichter2007/grub-customizer 
sudo apt update
sudo apt install grub-customizer
```

# [yt-dlp](https://github.com/yt-dlp/yt-dlp)
```
sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/sbin/yt-dlp
sudo chmod a+rx /usr/local/sbin/yt-dlp
sudo apt install ffmpeg
```

# [Node.js](https://nodejs.org/en/download)
```
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 22

# Verify the Node.js version:
node -v # Should print "v22.17.0".
nvm current # Should print "v22.17.0".

# Verify npm version:
npm -v # Should print "10.9.2".
```

# [Gemini CLI](https://github.com/google-gemini/gemini-cli)
## run CLI 
`npx https://github.com/google-gemini/gemini-cli`
## or just install it via
```
npm install -g @google-gemini/gemini-cli
gemini
```
