# Kubunto New Setup
# wifi not working
## probe with driver iwlwifi failed with error -110
```
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
- deattach power/battery
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

flatpak install flathub com.anydesk.Anydesk org.chromium.Chromium net.code_industry.MasterPDFEditor org.mozilla.firefox com.sublimetext.three org.videolan.VLC com.visualstudio.code

flatpak install flathub org.filezillaproject.Filezilla com.getpostman.Postman org.pgadmin.pgadmin4 tech.feliciano.pocket-casts org.sqlitebrowser.sqlitebrowser

flatpak run org.chromium.Chromium
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
[powerlevel10k/powerlevel10k](https://github.com/romkatv/powerlevel10k)
`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"`

`ZSH_THEME="powerlevel10k/powerlevel10k"`

## restart zsh
`exec zsh`
