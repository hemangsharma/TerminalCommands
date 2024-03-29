# TerminalCommands
This repository contains useful macOS terminal commands

## Unix Epoch Time
date +%s

## List All Mounted Drives
diskutil list

## Keeping Make awake
caffeinate 

## Add space to dock
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'

## Hide non-active apps in the dock
defaults write com.apple.dock static-only -bool TRUE

## Startup using power button only (Only Macs with power button)
sudo nvram AutoBoot=%00

## Final Cut Pro X trial reset
mv -v ~/Library/Application\ Support/.ffuserdata ~/.Trash

## Logic Pro trial reset
mv -v ~/Library/Application\ Support/.lpxuserdata ~/.Trash

## Change rows in Launchpad (replace 4 with desired number)
defaults write com.apple.dock springboard-rows -int 4

## Change columns in Launchpad (replace 4 with desired number)
defaults write com.apple.dock springboard-columns -int 4

## Reset Launchpad layout to default
defaults write com.apple.dock ResetLaunchPad -bool true <br>
defaults delete com.apple.dock springboard-rows <br>
defaults delete com.apple.dock springboard-columns

## Uninstall Java from macOS
sudo rm -fr /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin <br>
sudo rm -fr /Library/PreferencePanes/JavaControlPanel.prefPane <br>
sudo rm -fr ~/Library/Application\ Support/Oracle/Java <br>

## Reset Parallels
(!/bin/sh)
( Reset Parallels Desktop's trial and generate a casual email address to register a new user)<br><br>
rm /private/var/root/Library/Preferences/com.parallels.desktop.plist /Library/Preferences/Parallels/licenses.xml<br><br>
jot -w pdu%d@gmail.com -r 1

## Test network speed
```zsh
networkquality
