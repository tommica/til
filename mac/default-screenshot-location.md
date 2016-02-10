# Default Screenshot Location on OSX

By default OSX saves all screenshots to the desktop. You can change the location they get stored in with this:

```bash
mkdir ~/Desktop/Screenshots
defaults write com.apple.screencapture location ~/Desktop/Screenshots
killall SystemUIServer
```

[source](http://osxdaily.com/2011/01/26/change-the-screenshot-save-file-location-in-mac-os-x/)
