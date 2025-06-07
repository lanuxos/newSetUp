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
apt install synaptic curl golang-go htop net-tools nodejs transmission vlc

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