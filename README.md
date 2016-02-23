# ScreenChat

iOS Tweak for non-jailbroken devices for Snapchat

###Current features:
* Block screenshot detection
* Remove caption character limit
* Remove timer and timer UI

###Planned features:
* Saving to camera roll

#####Thanks to
* Giovanni Di Grezia, whose [code](http://www.xgiovio.com/blog-photos-videos-other/blog/resign-your-ios-ipa-frameworks-and-plugins-included/) served as the basis for the patchapp.sh revisions


This is a test, not a project for invading the privacy of users. I am not responsible for any uses of this code.

Requirements
============
* iOS device
* Apple Developer account or certificates
* XCode with iPhone SDK
* Decrypted ipa file of the app
* [optool](https://github.com/alexzielenski/optool/files/91118/optool.zip)
* [theos-jailed] (https://codeload.github.com/BishopFox/theos-jailed/zip/master)

How to install
============
* Uninstall Snapchat from the iOS device.
* Extract or download an Snapchat decrypted ipa file.
* Place an symlink in the project folder named `theos` pointing to the theos-jailed folder you downloaded: `ln -s /path/to/theos-jailed/ theos`
* Run `make package`
* Run `./patchapp.sh info /path/to/your/file.ipa`
* Take the information from that and use XCode to create a Provisioning Profile
* Run `.patchapp.sh patch /path/to/Snapchat.ipa BUNDLE_ID` to inject the tweak into the .ipa (get the BUNDLE_ID from the info command)
* Install the .mobileprovision to the device
* Install the ipa to the device
