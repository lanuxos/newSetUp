# ubuntu new set up

# update && upgrade
```bash
sudo apt update && apt upgrade -y
```

# install media codecs
```bash
sudo apt install ubuntu-restricted-extras
sudo apt install ubuntu-restricted-addons
```

# enable minimize on click
```bash
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

# install GNOME Tweak
```bash
sudo apt install gnome-tweaks
# if E: Unable to locate package gnome-tweaks
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo apt update
sudo apt install gnome-tweaks
```

# install GNOME shell extensions
```bash
sudo apt install gnome-shell-extensions
```

# install GNOME sushi
```bash
sudo apt install gnome-sushi
```

# install ubuntu cleaner
```bash
sudo add-apt-repository ppa:gerardpuig/ppa
sudo apt-get update
sudo apt-get install ubuntu-cleaner
```

# install synaptic
```bash
sudo apt install synaptic
```

# install flatpak
```bash
sudo add-apt-repository ppa:alexlarsson/flatpak
sudo apt update
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

# install wine
```bash
sudo apt-add-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ bionic main'
sudo apt-get install --install-recommends winehq-stable
```

# install net-tools
```bash
sudo apt install net-tools
```

# clean system
```bash
sudo apt autoclean
sudo apt autoremove
```