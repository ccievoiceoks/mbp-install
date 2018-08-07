# New Standard MBP Reinstallation

## --> From August 2018

* Reinstallation done with APFS and APFS Encrypted (APFS Only Selected)
* Mac OS High Sierra + Patch
* Activate FileVault on disk !!!!
* Intego Security Software 
* CleanMyMac 3
* 1Password 7
* Brew Install
	* Tree
	* Telnet
* Google Chrome
* pCloud Drive
* Synolody Drive Assistant
* Dropbox
* Code Runner
* Airmail 3
* Aperture
* Bartender 3
* Cardhop 
* ChatMate
	* FB Messenger
	* What's App
* Cisco Anyconnect
* Clarify --> Removed because not compliant with OS High Sierra
* Colors for Hue
* Comptes & Budget
* DB Browser for SQLite
* Divvy
* Dictionnaire
* Dx0 Perspective
* Dymo Label
* Epson Software
* Fantastical 2
* File Viewer
* Firefox
* ForkLift
* Github Desktop
* Go Pro Software
	* Fusion Studio
	* Quick 
	* VR Player
* HP Printing Software (HP 6830 Printer)
* iStats Menus
* iTerm2
* Livraisons
* Logitech Software (Keyboard)
* Marked 2
* iMovie
* iPhoto
* Monolingual
* Keynotes
* Paw
* PhotoLemur
* Postman
* Python 3.7
* Remoter
* RoyalTSX
* ScreenFlow
* Network Radar (Evaluation)
* Numbers
* Opera
* Sequel Pro
* Skitch
* Sonos
* Spotify
* Sublime Text 3
* TeamViewer
* The Unarchiver
* Time Machine
* TranslatorX
* TunnelBlick
* Tweetbot 3
* VLC
* VMWare Fusion
* Webex Teams
* VyprVPN
* Wifi Explorer
* Wireshark

**Additional Settings**

* General
	* **_Google Chrome_** Default Browser
	* Activate Menu and Dock for Dark mode !!!!
* Desktop
	* Random WallPaper every 30 minutes
	* Screensaver after 20 minutes
* Adapt Dock
	* Lower the size
	* Magnify the effect
* Language French ( Select order if problems with Airmail install !!!)
* Security 
	* Authorize iWatch to unlock
	* FileVault Activated (2password defined as generic password)
	* Confidentiality --> Calendar
	* Confidentiality --> Siri
	* Confidentiality --> Fantastical 2
	* Contacts --> Fantastical 2
	* Contacts --> VirusBarrier
	* Contacts --> Airmail
	* Calendar --> iStats Menu
	* Calendar --> Fantastical 2
	* Calendar --> Airmail
	* Rappels --> Fantastical 2
	* Rappels --> Airmail 
	* Accessibility --> Divvy
* Display
	* Configure Second screen LG to be the copy
	* Activate Night Shift from 21:30 up to 06:30
* Energy Saving
	* On Battery
		* Shutdown screen after 3 minutes
		* Suspend HD when possible
	* On Power 
		* Shutdown screen after 25 minutes
		* PowerNap Activated ---> ?????? To check
* Trackpad
	* Change sense of scrolling
* Printers
	* Epson ET4500 defined as default
	* HP 6830 all in one
* Sounds
	* Activate icon in taskbar
	* Activate Boom (Bluetooth) when home
* Bluetooth
	* Trackpad
	* Logitech KT811
	* Boom 2
* Share / Partage
	* Activate File sharing
	* Activate Remote Sessions
		* Oks
		* Admin
	* Activate Remote Destktop
		* Oks
* Date/Time
	* Charleroi Timezone
	* Annonce Time every 30 minutes
		* Audrey - French
		* Aurelie - French
		* Thomas - French
		* Allison - English
		* Ava - English
		* Samantha - English
		* Alex - English
		* Tom - English
		* Amelie - Canada
* Time Machine enabled and activate on Syno
* Fuse for pDrive
* Logitech

**!!! New Politics for Disk Management !!!**

> Do more Cloud and less local Disk savings
> In order to perform that
> pCloud and Synology Drive will be defined as new way of working
> Dropbox is slowly removed !
> 
> For Synology and DropBox , everything is stored in a new folder oks/Cloud Services/ (oks HomeFolder)
> 
> For pCloud , it is seen as an external drive

**New Things done on the network**

* Activate Synology DNS --> infra.ksiazek.be
* Activate Synology DHCP Server

#Still to do

- [X] Git
- [X] Dotfiles
- [ ] Sublime Packages
- [ ] Certificates ???


# Activate Subl shortcut

1. Create subfolfder $HOME/bin
2. Perform a link to application Sublime Test3
    ```bash
    ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" $HOME/bin/subl
    ```
    Pay Attention that we can't have the Sublime\ Text --> it should be replace by Sublime Text if using autocompletion
3. Edit the PATH in order to add $HOME/bin folder
    ```bash
    echo 'export PATH=$HOME/bin:$PATH' >> $HOME/.bash_profile
    ```
4. Perform a resource of the bash
    ```bash
    source $HOME/.bash_profile
    ```


# ~~Activate the dotfiles settings~~

~~1. Perform a backup of __.bash_profile__ (Here .bash_profile_beforedotfiles)~~
~~2. Copy settings .bash_profile from Matthias Fork~~ 
~~3. Copy settings from .bash_prompt in a new file from Matthias Fork~~
~~4. copy setting from .aliases in a new file from Matthias Fork~~
~~5. Adapt Now the fork with my settings !!!!~~
~~6. Put the 2 followings alias and comment some others~~
~~    * alias pcloud="cd $HOME/pCloud\ Drive/"~~
~~    * alias pcloudgit="cd $HOME/pCloud\ Drive/GitRepo/"~~

# New dotfiles settings

1. Create a new repo for dotfiles --> Mydotfiles on github
2. Create a new hidden folder in the $HOME --> .mydotfiles
3. Create an INITIAL BACKUP folder to store all initial files before we will change the config
4. Create also a .ssh folder in the INITIAL BACKUP folder
5. Move the initial file as backup in the INITIAL folder
    ```bash
    mv $HOME/.bash_profile $HOME/.mydotfiles/INITIAL-BACKUP-MBP-OKS/.bash_profile
    mv $HOME/.gitconfig $HOME/.mydotfiles/INITIAL-BACKUP-MBP-OKS/.gitconfig
    mv $HOME/.ssh/config $HOME/.mydotfiles/INITIAL-BACKUP-MBP-OKS/.ssh/config
    ```
6. As **.gitconfig** and **.ssh/config** files are static for the moment , copy back these 2 files in the root of .mydotfiles as they are config file for our setup
    ```bash
    cp $HOME/.mydotfiles/INITIAL-BACKUP-MBP-OKS/.gitconfig $HOME/.mydotfiles/.gitconfig
    cp $HOME/.mydotfiles/INITIAL-BACKUP-MBP-OKS/.ssh/config $HOME/.mydotfiles/.ssh/config
    ```
7. Create already symlinks for these 2 files:
    ```bash
    cd $HOME
    ln -sv $HOME/.mydotfiles/.gitconfig $HOME
    cd $HOME/.ssh
    ln -sv $HOME/.mydotfiles/.ssh/config $HOME/.ssh/config
    ```
8. Now we can continue with the remaining process of the dotfiles process, so in
the .mydotfiles folder , create all new files
    ```bash
    cd $HOME/.mydotfiles
    touch .aliases
    touch .bash_profile
    touch .bash_prompt
    ```
9. Updates these files --> .aliases , .bash_profile and .bash_prompt with the settings in the Fork of Matthias

10. Once it is done , create the symlinks to these files as before
    ```bash
    ln -sv $HOME/.mydotfiles/.aliases $HOME
    ln -sv $HOME/.mydotfiles/.bash_profile $HOME
    ln -sv $HOME/.mydotfiles/.bash_prompt $HOME
    ```

# More to come eventually

11. Launch the bash_profiles to reload settings
    ```bash
    cd $HOME
    source .bash_profile
    ```
# E