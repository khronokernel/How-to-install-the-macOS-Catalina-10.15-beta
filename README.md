# How-to-install-the-macOS-Catalina-10.15-beta

So you just watched the keynote from WWDC 2019 and you're itching to try it out on your hackintosh, well you've come to the right place.

# What you'll need

* macOS Developer Beta Access Utility(can be found at either [https://developer.apple.com/download/](https://developer.apple.com/download/) if you're a developer or if you're cheap you can get them for free at [betaprofiles](https://betaprofiles.com))
* An 8GB+ USB stick
* [mountEFI](https://github.com/corpnewt/MountEFI) or some other form of EFI mounting
* a Mac/Hackintosh running macOS to download Catalina
* A working hackintosh EFI(If you don't have one yet, follow the [Vanilla Guide](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/))
* A hack to test this on(duh)

# Getting macOS Catalina

So to start, you'll want to grab the macOS Developer Beta Access Utility and run it. What this does is whitelists our serial number to allow us to download macOS betas

Once the utility is done, you'll notice that you have a new update in system preferences being macOS 10.15. Download that and we can proceed to making the installer

# Preparing the USB

Next you'll want to format the USB as follows:

* Name: MyVolume
* Format: Mac OS Extended
* Scheme: GUID Partition map

# Creating the Installer

Quite simple, just run the following command in terminal:

    sudo /Applications/Install\ macOS\ 10.15\ Beta.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume

Next, we'll want to mount the USB's EFI partition by running [mountEFI](https://github.com/corpnewt/MountEFI) and then chucking our Hackintosh's EFI in. And now you're ready to boot! Keep in mind this is a beta so issues will pop up, and Clover may have issues with kennel injection so it's recommended to either wait or switch to OpenCore([Wrote a guide for anyone who's interested](https://khronokernel-1.gitbook.io/getting-started-with-opencore/))
