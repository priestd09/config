# Config

**Config** is a recipe to get a new Mac running from scratch, setup applications and developer environment. I use this repo to keep track of the important software and steps required to have a functioning system after a fresh install.

You are encouraged to fork this and modify it to your heart's content to match your own needs. **Please be sure to change your `.gitconfig` name and email address!**

## Install Software

The software selected is software that is "tried and true" --- software I need after any fresh install. I often install other software not listed here, but is handled in a case-by-case basis.

### Install from App Store

* [1Password](https://itunes.apple.com/app/1password-password-manager/id443987910?mt=12)
* [Fantastical](https://itunes.apple.com/app/fantastical-2-calendar-reminders/id975937182?mt=12)
* [Slack](https://itunes.apple.com/app/slack/id803453959?mt=12)
* [The Unarchiver](https://itunes.apple.com/app/the-unarchiver/id425424353?mt=12)
* [Xcode](https://itunes.apple.com/app/xcode/id497799835?mt=12)

### Install from Third-Party Websites

* Browsers
	* Chrome (installed via Cask)
	* [Firefox](http://firefox.com)
	* Opera (installed via App Store)

* Development
	* [GitHub Desktop](http://mac.github.com)
	* [Sublime Text 3](http://www.sublimetext.com/3)

* Utilities
	* [Dropbox](https://www.dropbox.com/install2)
	* [Skype](http://www.skype.com/en/download-skype/skype-for-computer/)
	* [Spotify](https://www.spotify.com/us/download/mac/)
	* [XtraFinder](https://www.trankynam.com/xtrafinder/)

# Xcode Command Line Tools

`Xcode > Preferences > Downloads > Command Line Tools`

# OS X Preferences

```bash

#Add a context menu item for showing the Web Inspector in web views
defaults write NSGlobalDomain WebKitDeveloperExtras -bool true

#Show the ~/Library folder
chflags nohidden ~/Library

#Store screenshots in subfolder in Dropbox
mkdir ~/Dropbox/Screenshots
defaults write com.apple.screencapture location ~/Desktop/Screenshots

#Delete Recent Items for VLC:
defaults delete org.videolan.vlc.LSSharedFileList RecentDocuments

#Disable listing recent items for VLC in the future:
defaults write org.videolan.vlc NSRecentDocumentsLimit 0
defaults write org.videolan.vlc.LSSharedFileList RecentDocuments -dict-add MaxAmount 0
```

# Sublime Text

Settings
--------

**Sublime Text > Preferences > Settings - User**

```json
{
	"bold_folder_labels": true,
	"close_windows_when_empty": true,
	"color_scheme": "Packages/User/SublimeLinter/Flatland Dark (SL).tmTheme",
	"fade_fold_buttons": false,
	"font_size": 12,
	"highlight_line": true,
	"highlight_modified_tabs": true,
	"ignored_packages":
	[
		"Vintage"
	]
}
```