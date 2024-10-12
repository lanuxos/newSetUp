# mac initial set up

# iTerm2
- oh-my-zsh installation
```bash
# installation via curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
# installation via wget
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"

```
- oh-my-zsh plugins
  - zsh-syntax-highlighting
  ```zsh
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```
  - ZSH-AutoSuggestion
  ```zsh
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```
  - 
- oh-my-zsh theme
  - powerlevel10k
  ```zsh
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
  ```
    - configuration
  ```zsh
  p10k configure
  ```
- .zsh
  [.zshrc](https://github.com/lanuxos/zshrc.git)

# update
```zsh
softwareupdate --list # or softwareupdate -l
sudo softwareupdate -i UPDATE_PKG_NAME
```

# install command line tools (CLT)
```zsh
xcode-select --install
```

# install homebrew
```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

# install brew packages
```zsh
brew install dart git htop mongodb-community mongodb-database-tools mongosh nmap node speedtest-cli thefuck tldr wget youtube-dl zsh
```

```zsh
brew install --cask iterm2 airdroid alfred android-file-transfer android-studio anydesk authy avast-security db-browser-for-sqlite docker droidid firefox google-chrome keepassxc mamp mongodb-compass-isolated-edition mysqlworkbench postman rectangle sequel-pro spectacle sublime-text teamviewer the-unarchiver thonny transmission unified-remote vlc virtualbox visual-studio-code wechat whatsapp foobar2000
```

# install applications
```
Adobe
Amphetamine.app
AppManager.app
FileZilla.app
Fritzing.app
Keynote.app
Laplock.app
Numbers.app
Pages.app
Python
Who's On My WiFi.app
wireshark
```

# system preferences customization
- General
  - Appearance > Dark
  - Highlight color > Graphite
  - Default web browser > Google Chrome
- Desktop & Screen Saver
- Dock & Menu Bar
- Users & Groups > Login items
- Keyboard
- Trackpad
- Sharing

# Start mac in verbose mode
```zsh
sudo nvram boot-args="-v"
```

# show all files in Finder
```zsh
defaults write com.apple.finder AppleShowAllFiles TRUE
killall Finder
```

# change screen shot file type [PNG/JPG]
```zsh
defaults write com.apple.screencapture type PNG
```

# show directory path on finder title
```zsh
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
killall Finder
```

# Erase Free Hard Dirve Space Securely
```zsh
diskutil secureErase freespace 3/Volumes/HARD_DRIVE_NAME
```

# Reset/sort Launchpad
```zsh
defaults write com.apple.Dock ResetLaunchPad -bool TRUE && killall Dock
```

# Enable copy text from Quick Look
```zsh
defaults write com.apple.finder QLEnableTextSelection -bool TRUE && killall Finder
```

# preventing mac from sleep
```zsh
caffeinate -t 3600
```

# brewing
```zsh
brew update && brew upgrade && brew cleanup && brew doctor
```

# Key Combinations
- Command (⌘)-R: Start up from the built-in macOS Recovery system. Or use Option-Command-R or Shift-Option-Command-R to start up from macOS Recovery over the internet. macOS Recovery installs different versions of macOS, depending on the key combination you use.
- Option (⌥) or Alt: Start up to Startup Manager, which allows you to choose other available startup disks or volumes.
- Option-Command-P-R: Reset NVRAM or PRAM.
```bash
nvram -c
```
- Shift (⇧): Start up in safe mode.
- D: Start up to the Apple Diagnostics utility. Or use Option-D to start up to this utility over the internet.
- N: Start up from a NetBoot server, if your Mac supports network startup volumes. To use the default boot image on the server, press and hold Option-N instead.
- Command-S: Start up in single-user mode. Disabled in macOS Mojave or later.
- T: Start up in target disk mode.
- Command-V: Start up in verbose mode.
- Eject (⏏) or F12 or mouse button or trackpad button: Eject removable media, such as an optical disc.
- Shift, Option, and Control keys on the left side and press the power button and hold all of these down for 10 seconds: Reset SMC.
