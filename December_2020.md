# New Installation December 2020

* Disable Licenses on Software where there is a count
  * Intego Security
  * Istat Menu
  * ScreenFlow
  * ...
* Disable Disk Security with Utility Disk ( Boot at Startup with Cmd+R) and disable the option in the menu to no Security to startup with external drive and on the drive

* Create Bootable Disk with New MacOS ( CLI Commands)

* Install New MacOS --> Big Sur, this Time

User Definition will define the ~ folder
Olivier <> Oks

> ### MANUAL 
> * Install 1Password ( via Portal , install app and code )
> * Install Intego Security ( Download on Website)
>   * Activate License
>   * Authorize Component in the System Security Tab
>   * Configure Network ( Home)
>   * Schedule a complete scan each day
>   * ...
> * Epson Software
> * Dymo
> * Sonos
> * TranslatorX
> * unifi ubiquity ===> Not Needed anymore as I have a controller



* Activate FileVault if it is not the case
* Store the Password Disk Encryption / Access in the Keychain Access
* Activate Apple Watch to accept request

* Install Xcode (via CLI)
```bash (sudo) xcode-select --install ```

* Configure the port in the correct vlan for Ethernet
* Configure Home Wifi Network

* Configure the Applications Icons in the TaskBar
* Configure Keyboard
* Configure Trackpad
* Configure Bluetooth Icon in upper Taskbar

* Install Homebrew
> Homebrew website is [Homebrew](https://brew.sh/index_fr)
> Brew update

* Install Brew packages
```zsh brew install << package>>```
 * openssh
 * moreutils
 * findutils
 * coreutils
 * dos2unix
 * nmap
 * ssh-copy-id
 * c-ares
 * docbook
 * docbook-xsl
 * freetype
 * xmlto
 * gettext
 * git
 * lua
 * luarocks
 * mackup
 * mas
 * ncurses
 * neofetch
 * ruby
 * stow
 * qmk/qmk/qmk (**error**)
 * lsd
 * macpilot
 * tree
 * telnet
 * nodejs
 * htop
 * cask
 * fzf
 * mysql-client
 * openssl
 * sqlite
 * tmux
 * wget
 * zsh
 * zsh-completions
 * zsh-syntax_highlighting
    sudo rm -rf /usr/local/Cellar/zsh-syntax-highlighting/0.7.1
 * antigen
 
 # Remove outdated versions from the cellar.
brew cleanup
 
 
 olivier@MacBook-Pro-de-Olivier ~ % python3 -m pip install --upgrade pip

* create new dotfiles folder
>> mkdir .oksdotfiles

```zsh mv ~/.config ~/.oksdotfiles/ ```
```zsh ln -s ~/.oksdotfiles/.config ~/.config ```
 
* brew install --cask ( different packages)
 * 1password
 * 1password-cli
 * cleanmymac
 * font-meslo-lg
 * osxfuse
 * alfred
 * rectangle
 * vyprvpn
 * bartender
 * webex-teams
 * royal-tsx
 * screenflow
 * brave-browser
 * sequel-pro
 * cheatsheet
 * spotify
 * devdocs
 * sublime-text
 * fantastical
 * the-unarchiver
 * firefox
 * visual-studio-code
 * forklift
 * vmware-fusion
 // * fuse ===> A Oublier c' est plutot OSXFUSE
 ln -svfhn ~/.oksdotfiles/.fuse ~/.fuse
 * google-chrome
 * iina
 * wireshark
 * istat-menus
 * keka
 * iterm2
 * logitech-presentation ==> To check how to continue
 * monolingual
 * ngrok
 * opera
 * paw
 * postman
 * docker
 * powershell
 * vagrant
 * microsoft-teams
 * whatsapp
 * microsoft-edge
 * microsoft-office
 * vagrant-manager
 * ssh-config-editor
   ==> Move config to dotfile or not / or with an exception !!!
 * cisco-proximity ----> Not needed
 * cisco-jabber ---> To see
 * aws-vpn-client
 * db-browser-for-sqlite
 * github
 * 
 * timemachineeditor
 * qlcolorcode
 * qlimagesize
 * qlmarkdown
 * qlstephen
 * quicklook-json
   
 
 
* installation with mas

mas signin is not anymore possible , perform a login via GUI
The App ID are not changing so we can create a list of ID

* mas search "Wifi Explorer"
mas install 494803304
* mas search numbers
mas install 409203825
* mas search "Comptes et Budget"
mas install 1269586528
* mas search "Keynote"
mas install 409183694
* mas search "Imovie" ?????
mas install 408981434
* mas search "Parcel"
mas install 639968404
* mas search Remoter
mas install 486899236
* mas search Tweetbot
mas instal 1384080005
* mas search Marked 2
mas install 890031187
* mas search "Chatmate for Whats'App "
mas install 1228059008
* mas search Airmail
mas install 918858936
* mas search "Pages"
mas install 409201541
* mas search "Chatmate for Facebook"
mas install 1249947725
* mas search "Colors for Hue " ??????
mas install 581915465
* mas search "GarageBand" ????
mas install 682658836
* mas search "Divvy" ???? replaced by rectangle
mas install 413857545
* mas search Cardhop
mas install 1290358394
* mas search Livraisons
mas install 924726344
* mas search "Step Two"
mas install 1448916662.  ====> May be in manual mode

mas instal 1384080005  Tweetbot

## Parameters changed

### There is a parameter which is changing the appearance of Applications Folder --> App.APP
sudo nvram SystemAudioVolume=" "
defaults write NSGlobalDomain NSTableViewDefaultSizeMode -int 2
defaults write NSGlobalDomain AppleShowScrollBars -string "Always"
defaults write NSGlobalDomain NSUseAnimatedFocusRing -bool false
defaults write NSGlobalDomain NSWindowResizeTime -float 0.001
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true
defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode2 -bool true
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true
defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true
defaults write com.apple.print.PrintingPrefs "Quit When Finished" -bool true
defaults write com.apple.LaunchServices LSQuarantine -bool false
defaults write NSGlobalDomain NSDisableAutomaticTermination -bool true

sudo defaults write /Library/Preferences/com.apple.loginwindow AdminHostInfo HostName


???? sudo pmset -a displaysleep 15 ???

defaults write com.apple.screensaver askForPassword -int 1
defaults write com.apple.screensaver askForPasswordDelay -int 0
defaults write com.apple.screencapture disable-shadow -bool true
defaults write com.apple.finder ShowExternalHardDrivesOnDesktop -bool true
defaults write com.apple.finder ShowHardDrivesOnDesktop -bool true
defaults write com.apple.finder ShowMountedServersOnDesktop -bool true
defaults write com.apple.finder ShowRemovableMediaOnDesktop -bool true
defaults write NSGlobalDomain AppleShowAllExtensions -bool true   ====> Bingo this one is not correct
defaults write com.apple.finder ShowStatusBar -bool true
defaults write com.apple.finder ShowPathbar -bool true
defaults write com.apple.finder _FXShowPosixPathInTitle -bool true
defaults write NSGlobalDomain com.apple.springing.enabled -bool true
defaults write NSGlobalDomain com.apple.springing.delay -float 0
defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool true
defaults write com.apple.desktopservices DSDontWriteUSBStores -bool true
defaults write com.apple.finder FXPreferredViewStyle -string "Nlsv"
chflags nohidden ~/Library && xattr -d com.apple.FinderInfo ~/Library
sudo chflags nohidden /Volumes
defaults write com.apple.finder FXInfoPanesExpanded -dict \
        General -bool true \
        OpenWith -bool true \
        Privileges -bool true
defaults write com.apple.dock tilesize -int 36
defaults write com.apple.dock minimize-to-application -bool true
defaults write com.apple.dock show-process-indicators -bool true
defaults write com.apple.dock autohide-delay -float 0
defaults write com.apple.dock autohide-time-modifier -float 0
defaults write com.apple.dock show-recents -bool false
defaults write com.apple.terminal StringEncodings -array 4
defaults write com.googlecode.iterm2 PromptOnQuit -bool false
defaults write com.apple.appstore ShowDebugMenu -bool true
defaults write com.apple.SoftwareUpdate AutomaticCheckEnabled -bool true
defaults write com.apple.SoftwareUpdate ScheduleFrequency -int 1
defaults write com.apple.SoftwareUpdate AutomaticDownload -int 1
defaults write com.apple.SoftwareUpdate CriticalUpdateInstall -int 1
defaults write com.apple.commerce AutoUpdate -bool true
defaults write com.apple.commerce AutoUpdateRestartRequired -bool true
defaults write com.google.Chrome PMPrintingExpandedStateForPrint2 -bool true
defaults write com.google.Chrome.canary PMPrintingExpandedStateForPrint2 -bool true
defaults write com.operasoftware.Opera PMPrintingExpandedStateForPrint2 -boolean true
defaults write com.operasoftware.OperaDeveloper PMPrintingExpandedStateForPrint2 -boolean true
 
mas instal 1384080005



Install Manually PCLOUD-DRIVE

Good reference for settings
https://pawelgrzybek.com/change-macos-user-preferences-via-command-line/

