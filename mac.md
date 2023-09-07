# mac initial set up

# update
```
softwareupdate --list # or softwareupdate -l
sudo softwareupdate -i UPDATE_PKG_NAME
```

# install command line tools (CLT)
`xcode-select --install`

# install homebrew
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

# install brew packages
`brew install dart git htop mongodb-community mongodb-database-tools mongosh nmap node speedtest-cli thefuck tldr wget youtube-dl zsh`

`brew install --cask iterm2 airdroid alfred android-file-transfer android-studio anydesk authy avast-security db-browser-for-sqlite docker droidid firefox google-chrome keepassxc mamp mongodb-compass-isolated-edition mysqlworkbench postman rectangle sequel-pro spectacle sublime-text teamviewer the-unarchiver thonny transmission unified-remote vlc virtualbox visual-studio-code wechat whatsapp foobar2000`

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

# show all files in Finder
```
defaults write com.apple.finder AppleShowAllFiles TRUE
killall Finder
```

# change screen shot file type [PNG/JPG]
`defaults write com.apple.screencapture type PNG`

# show directory path on finder title
```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
killall Finder
```

# Erase Free Hard Dirve Space Securely
`diskutil secureErase freespace 3/Volumes/HARD_DRIVE_NAME`

# Reset/sort Launchpad
`defaults write com.apple.Dock ResetLaunchPad -bool TRUE && killall Dock`

# Enable copy text from Quick Look
`defaults write com.apple.finder QLEnableTextSelection -bool TRUE && killall Finder`

# preventing mac from sleep
`caffeinate -t 3600`

# brewing
`brew update && brew upgrade && brew cleanup && brew doctor`

# iTerm2
- oh-my-zsh installation
```
# installation via curl
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
# installation via wget
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"

```
- oh-my-zsh plugins
  - zsh-syntax-highlighting
  `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
  - ZSH-AutoSuggestion
  `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
  - 
- oh-my-zsh theme
  - powerlevel10k
  `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
    - configuration
  `p10k configure`
- .zsh