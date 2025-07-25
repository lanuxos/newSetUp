# Linux Mint New Setup

# update
```
apt update
apt fullupgrade
apt autoclean
apt autoremove
```

# apt
```
apt install synaptic curl catfish copyq git golang-go htop net-tools nodejs numlockx python3-pip python3-setuptools python3-venv stacer thefuck transmission vlc

apt install darktable gimp inkscape libreoffice openshot-qt postgresql postgresql-contrib
```

# flatpak

```
flatpak install flathub org.chromium.Chromium

flatpak install flathub com.anydesk.Anydesk org.chromium.Chromium net.code_industry.MasterPDFEditor org.mozilla.firefox org.videolan.VLC

flatpak install flathub org.filezillaproject.Filezilla com.getpostman.Postman org.pgadmin.pgadmin4 com.sublimetext.three tech.feliciano.pocket-casts org.sqlitebrowser.sqlitebrowser
```

# [code](https://code.visualstudio.com/docs/setup/linux)
```
sudo apt update
sudo apt install wget gpg
echo "code code/add-microsoft-repo boolean true" | sudo debconf-set-selections
sudo apt-get install wget gpg
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
- log out, and re-login

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
```bash
sudo cp ./*.ttf /usr/local/share/fonts
sudo fc-cache -f -v
```
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

# disable last-access-time on SSD
```
sudo nano /etc/fstab
# add 'noatime'
# UUID=xxxx /               ext4    errors=remount-ro 0
# UUID=xxxx /               ext4    noatime,errors=remount-ro 0
systemctl status fstrim
# if not, activate timer to schedule execute
sudo systemctl enable fstrim.timer && sudo systemctl start fstrim.timer
```

# reduce swap auto launch, use swap when ram used up to 80% [default 40%]
```
sudo xed /etc/sysctl.config
# go to last line and add
# vm.swappiness=20
```

# ulauncher
`sudo add-apt-repository universe -y && sudo add-apt-repository ppa:agornostal/ulauncher -y && sudo apt update && sudo apt install ulauncher`

# [Microsoft Fonts](http://ftp.us.debian.org/debian/pool/contrib/m/msttcorefonts/ttf-mscorefonts-installer_3.8.1_all.deb)
```
sudo apt install ./ttf-mscorefonts-installer_3.8.1_all.deb
sudo cp -v -r /usr/share/fonts/truetype/msttcorefonts /usr/local/share/fonts/msttcorefonts2
sudo apt-get purge ttf-mscorefonts-installer
sudo dpkg-reconfigure fontconfig

```

