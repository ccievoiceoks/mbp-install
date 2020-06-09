# Brew installed
oks@MBP2020 ~ % brew list
c-ares			gmp			libev			libpng			lua			openexr			ruby			utf8proc
docbook			gnu-getopt		libevent		libsmi			lua@5.1			openjpeg		screenresolution	webp
docbook-xsl		gnutls			libffi			libssh			luarocks		openssl@1.1		shared-mime-info	wireshark
freetype		ilmbase			libgcrypt		libtasn1		mackup			p11-kit			sqlite			x265
gdbm			imagemagick		libgpg-error		libtiff			mas			pcre			stow			xmlto
gettext			jansson			libheif			libtool			ncurses			pcre2			telnet			xz
ghostscript		jemalloc		libidn2			libunistring		neofetch		python			tmux
git			jpeg			libmaxminddb		libyaml			nettle			python@3.8		tree
glib			libde265		libomp			little-cms2		nghttp2			readline		unbound
oks@MBP2020 ~ %

# Brew cask installed

oks@MBP2020 ~ % brew cask list
alfred                   devdocs                  fuse                     iterm2                   opera                    royal-tsx                sublime-text             vyprvpn
bartender                fantastical              google-chrome            logitech-presentation    paw                      screenflow               the-unarchiver           webex-teams
brave-browser            firefox                  iina                     monolingual              postman                  sequel-pro               visual-studio-code       wireshark
cheatsheet               forklift                 istat-menus              ngrok                    rectangle                spotify                  vmware-fusion
oks@MBP2020 ~ %

# Mas List installed

oks@MBP2020 ~ % mas list
494803304 WiFi Explorer (2.6)
409203825 Numbers (6.2.1)
1269586528 Comptes-et-Budget (7.0.22)
409183694 Keynote (9.2.1)
408981434 iMovie (10.1.14)
639968404 Parcel (6.3.7)
486899236 Remoter (6.0.1)
1384080005 Tweetbot (3.3.3)
890031187 Marked 2 (2.5.40)
1228059008 ChatMate for WhatsApp (4.3.1)
918858936 Airmail (4.0.7)
409201541 Pages (10.0)
1249947725 ChatMate for Facebook (4.3.1)
581915465 Colors for Hue (1.2.7)
682658836 GarageBand (10.3.4)
413857545 Divvy (1.5.2)
1290358394 Cardhop (1.3.4)
924726344 Livraisons (3.2.2)
oks@MBP2020 ~ %


# Settings Changed

Last login: Wed May 27 20:35:45 on ttys000
oks@MBP2020 ~ %
oks@MBP2020 ~ %
oks@MBP2020 ~ % sudo nvram SystemAudioVolume=" "
Password:
oks@MBP2020 ~ % defaults write NSGlobalDomain NSTableViewDefaultSizeMode -int 2
oks@MBP2020 ~ % defaults write NSGlobalDomain AppleShowScrollBars -string "Always"
oks@MBP2020 ~ % defaults write NSGlobalDomain NSUseAnimatedFocusRing -bool false
oks@MBP2020 ~ % defaults write NSGlobalDomain NSWindowResizeTime -float 0.001
oks@MBP2020 ~ % defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode2 -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true
oks@MBP2020 ~ % defaults write com.apple.print.PrintingPrefs "Quit When Finished" -bool true
oks@MBP2020 ~ % defaults write com.apple.LaunchServices LSQuarantine -bool false
oks@MBP2020 ~ % defaults write NSGlobalDomain NSDisableAutomaticTermination -bool true
oks@MBP2020 ~ % sudo defaults write /Library/Preferences/com.apple.loginwindow AdminHostInfo HostName
Password:
oks@MBP2020 ~ % defaults write NSGlobalDomain NSAutomaticDashSubstitutionEnabled -bool false
oks@MBP2020 ~ % defaults write NSGlobalDomain NSAutomaticPeriodSubstitutionEnabled -bool false
oks@MBP2020 ~ % defaults write NSGlobalDomain NSAutomaticQuoteSubstitutionEnabled -bool false
oks@MBP2020 ~ % defaults write com.apple.BluetoothAudioAgent "Apple Bitpool Min (editable)" -int 40
oks@MBP2020 ~ % sudo defaults write /Library/Preferences/com.apple.loginwindow showInputMenu -bool true
oks@MBP2020 ~ % sudo pmset -a displaysleep 15
Warning: Idle sleep timings for "Battery Power" may not behave as expected.
- Display sleep should have a lower timeout than system sleep.
oks@MBP2020 ~ % defaults write com.apple.screensaver askForPassword -int 1
oks@MBP2020 ~ % defaults write com.apple.screensaver askForPasswordDelay -int 0
oks@MBP2020 ~ % defaults write com.apple.screencapture disable-shadow -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowExternalHardDrivesOnDesktop -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowHardDrivesOnDesktop -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowMountedServersOnDesktop -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowRemovableMediaOnDesktop -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain AppleShowAllExtensions -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowStatusBar -bool true
oks@MBP2020 ~ % defaults write com.apple.finder ShowPathbar -bool true
oks@MBP2020 ~ % defaults write com.apple.finder _FXShowPosixPathInTitle -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain com.apple.springing.enabled -bool true
oks@MBP2020 ~ % defaults write NSGlobalDomain com.apple.springing.delay -float 0
oks@MBP2020 ~ % defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool true
oks@MBP2020 ~ % defaults write com.apple.desktopservices DSDontWriteUSBStores -bool true
oks@MBP2020 ~ % defaults write com.apple.finder FXPreferredViewStyle -string "Nlsv"
oks@MBP2020 ~ % chflags nohidden ~/Library && xattr -d com.apple.FinderInfo ~/Library
oks@MBP2020 ~ % sudo chflags nohidden /Volumes
oks@MBP2020 ~ % defaults write com.apple.finder FXInfoPanesExpanded -dict \
        General -bool true \
        OpenWith -bool true \
        Privileges -bool true
oks@MBP2020 ~ % defaults write com.apple.dock tilesize -int 36
oks@MBP2020 ~ % defaults write com.apple.dock minimize-to-application -bool true
oks@MBP2020 ~ % defaults write com.apple.dock show-process-indicators -bool true
oks@MBP2020 ~ % defaults write com.apple.dock autohide-delay -float 0
oks@MBP2020 ~ % defaults write com.apple.dock autohide-time-modifier -float 0
oks@MBP2020 ~ % defaults write com.apple.dock show-recents -bool false
oks@MBP2020 ~ % defaults write com.apple.terminal StringEncodings -array 4
oks@MBP2020 ~ % defaults write com.googlecode.iterm2 PromptOnQuit -bool false
oks@MBP2020 ~ % defaults write com.apple.appstore ShowDebugMenu -bool true
oks@MBP2020 ~ % defaults write com.apple.SoftwareUpdate AutomaticCheckEnabled -bool true
oks@MBP2020 ~ % defaults write com.apple.SoftwareUpdate ScheduleFrequency -int 1
oks@MBP2020 ~ % defaults write com.apple.SoftwareUpdate AutomaticDownload -int 1
oks@MBP2020 ~ % defaults write com.apple.SoftwareUpdate CriticalUpdateInstall -int 1
oks@MBP2020 ~ % defaults write com.apple.commerce AutoUpdate -bool true
oks@MBP2020 ~ % defaults write com.apple.commerce AutoUpdateRestartRequired -bool true
oks@MBP2020 ~ % defaults write com.google.Chrome PMPrintingExpandedStateForPrint2 -bool true
oks@MBP2020 ~ % defaults write com.google.Chrome.canary PMPrintingExpandedStateForPrint2 -bool true
oks@MBP2020 ~ % defaults write com.operasoftware.Opera PMPrintingExpandedStateForPrint2 -boolean true
oks@MBP2020 ~ % defaults write com.operasoftware.OperaDeveloper PMPrintingExpandedStateForPrint2 -boolean true
oks@MBP2020 ~ %
