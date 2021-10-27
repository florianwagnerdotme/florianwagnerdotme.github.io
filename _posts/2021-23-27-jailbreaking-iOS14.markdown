---
layout: post
title:  "Getting started with iOS app hacking - escape the prison!"
date:   2021-10-27 12:00:00 +0200
categories: mobile app hacking, iOS hacking
---
Like in my [introduction article][easierDoneThanSaid] said, the following will get you started with hacking iOS Apps. First things first, to  get started you will need something to install and test your app of choice. While on Android there are emulators that are emulating CPU instruction sets very well and allow an almost native experience in comparison to a real Android device this is different on iOS. The only company I am aware of that is offering a remote conntection to an iOS virtual device is [Corellium][corellium]. I personally have not tried their services thats why I can´t tell you if their virtual iOS experience has any downfalls in terms of security tests. I could imagine that a virtual iOS environment can be very interesting and useful for security automation.    
My recommended way to start is to perform security tests on a real iOS device.  
Due to the long support of devices by Apple it is very easy to get your hands on a test device. For this I would recommend you to buy a **used** iPhone between iPhone 6s to iPhone X or the iPad equivalent with an installed software version in between iOS 12.0 to 14.7.1. Maybe you even hoard your old iPhone somewhere - then get it out now!    

Why these recommendations?  
  
1. iPhones and iPads are easy and cheap to get online, especially used (you get the iPhone 6s from 30-100 bucks). 
2. The easiest and most reliable jailbreak currently available works on them (see [checkra1n][checkra1n]). 
3. You do something good for the environment in reusing an old device and giving it a new purpose. ;-)
4. With a buyers/sellers contract you can even take used devices off your taxes (e.g. for an educational purpose)!

# [checkra1n][checkra1n], a remarkable jailbreak

The jailbreak we will use to break free our iPhone within this article is checkra1n. Like mentioned, checkra1n is one of the easiest and most reliable jailbreaks ever released. Its base is a bug found within the Boot ROM (aka SecureROM), the first code that is running when starting up an iOS device. Because of this and the fact that the Boot ROM is designed to be read only, Apple is and will never be able to patch this bug within the vulnerable devices.  
On top of this checkra1n is a semi-tethered jailbreak, which means that it only persists until the next reboot of the device which makes it really easy to remove.
While checkra1n has many advantages for security researchers and penetration testers it is **NOT recommended** to install any jailbreak on your primary device. Jailbreaking your device will remove main security restrictions by Apple and makes attacking your device much easier. checkra1n undermines the trust of the iOS secure boot chain and will allow attackers to gain easy access and privilege escallation. My recommendation for all of you who wonder how they can protect themself is, if you can afford it, get an iOS Device with an A12 CPU or higher. As another countermeasure restart your device every time after you have left it unattended.  

![News report: iPhone Jailbreak by Florian Wagner]({{ site.url }}/assets/article2/iPhoneInJail.png){: .center-image}

"News report: iPhone Jailbreak" illustrated by Florian Wagner - [CC BY-NC-ND 4.0][cc] 04/10/21  

#Requirements for the checkra1n jailbreak
  
To jailbreak you iOS device you will need a device to execute the [checkra1n][checkra1n] application from. If you have a notebook or desktop PC with Linux ready to go, this is time to get the engine started. MS Windows is currently not supported by the checkra1n authors - I would recommand you either try to execute the script with the [Windows Subsystem for Linux][WSL] (I have never tested this) or to create a bootable usb stick with e.g. [Ubuntu][ubuntu] and execute checkra1n from the live system. Due to the handling of USB device in virtual machines jailbreaking your iDevice will not work out of a Unix virtual machine.
On native MacOS you will not have any problem to follow my instructions. On Linux you have to download the bash script and run it within the terminali (don`t forget to give it execution permissions ;-) beginning with step 10 below the steps are identical. For an easier follow along I have listed the steps to jailbreak your iPhone/iPad below. What I show you has been successfully tested on my Macbook with MacOS Monterey 12.0.1 and my iPhone 6s with iOS 14.7.1 installed.

# Hints and disclaimer:
 
* You will need a USB type A to lightning cable to directly connect your iPhone/iPad to your computer (USB C to ligning cables are from my experience not working). 
* Notice that this will not work with any kind of docking station, it has to be the USB A to lightning cable connect directly from your computer to the iDevice. 
* If you do this with an iPhone 8s up to the iPhone X you have to activate the "Skip A11 BPR check" (open checkra1n app --> Options --> activate "Skip A11 BPR check"), before starting the Jailbreak process. Other then that you can follow along the process like discribed below. 
* Make sure that your phone has enough charge before you try this - 50% should be enough.
* Prior execution of the steps below make sure that you deactivate the pin/passcode/touchID/FaceID login.
* Again, please do not use your productivly used iDevice for this. Jailbreaking our iDevice removes important security restrictions from your phone. 
* checkra1n is a semi-tethered jailbreak variant which means that it will last until the device restarts.
* Take note that jailbreaking your iOS device with this method can be reversed but that I will not take any responsibility for any damage to your devices that might occure. Do your research aside from this article and make sure that you understand what you do before taking any action.
* All techniques provided in my articles are solely meant for educational purposes. Do not use any of this information other then for ethical hacking, own research or personal use. 

# Jailbreaking iOS 12.0-14.7.1 with checkra1n

1. Downlaod the latest version of checkra1n from their offical website (step 1): [https://checkra.in][checkra1n] --> "Get the beta now" - make a selection for the installer based on your environment.  
![checkra1n website]({{ site.url }}/assets/article2/1checkra1nWebsite.png){: .center-image}

2. Click on "Download for macOS", optionally check the downloaded installer against malware with your antivirus of choise (if at all only "MacOS:Jailbreak-BI" should pop up, which is ok) and check the integrity by comparing the provided SHA256 hash displayed at step 2.
3. Save the installer locally.

![checkra1n download]({{ site.url }}/assets/article2/2checkra1nDownload.png){: .center-image}

4. Install checkra1n on macOS by opening it from your desktop.
5. Drag the application into the application's folder.

![checkra1n installation]({{ site.url }}/assets/article2/3checkra1nInstallation.png){: .center-image}

6. Open your macOS "System Preferences", go to "Security & Privacy" and click on "Click the lock to make changes.".
7. After providing your password you can click on "Open Anyway" to allow the execution of "checkra1n" even though it could not be identified.   

![checkra1n security exception]({{ site.url }}/assets/article2/4checkra1nSecurityException.png){: .center-image}

8. Confirm your choice by clicking on "Open".

![checkra1n security exception]({{ site.url }}/assets/article2/5checkra1nSecurityException.png){: .center-image}

9. With your iPhone connected over USB you will now presented with the start screen of checkra1n.

![checkra1n first start]({{ site.url }}/assets/article2/6checkra1nOpenedWithiPhoneConnected.png){: .center-image}

10. Getting your iPhone ready by starting it into DFU mode. On iPhone 6s you have to press and hold the power button + home button until you are in DFU mode.

![checkra1n DFU mode]({{ site.url }}/assets/article2/7checkra1niPhoneDFUMode.png){: .center-image}

11. Next start the app and click on "Options".

![checkra1n Options]({{ site.url }}/assets/article2/8checkra1nOptions.png){: .center-image}

12. If you have your device already updated to iOS 14.7.1 (and if something is not working) select the first option. Activate the verbose mode to see a wall of text while checkra1n gets executed (more or less only because it looks neat :-)
13. For all of you who are doing this with an iPhone 8s up to X, you have to select this option too.
14. After everything is selected, click on "Back".

![checkra1n Options]({{ site.url }}/assets/article2/9checkra1nOptionSelection.png){: .center-image}

15. You can now click on "Start" to start checkra1n.

![checkra1n Options]({{ site.url }}/assets/article2/10checkra1nStart.png){: .center-image}

16. Read the instructions displayed and follow them for your device to go into DFU (if not happend already) and execute the checkra1n payload. I have set mine already into DFU mode because I have made experience that his is working better.

![checkra1n Options]({{ site.url }}/assets/article2/11checkra1nStart.png){: .center-image}

17. After you have executed the steps successfully it should look like this. Your device should now boot up with a wall of text, indicating the execution of checkra1n.

![checkra1n Options]({{ site.url }}/assets/article2/12checkra1nBoot.png){: .center-image}

18. Finally you get a message that the everything is done and you can click on "Done" to close the window.

![checkra1n Options]({{ site.url }}/assets/article2/13checkra1nDone.png){: .center-image}

19. On your phone you should now see an app installed with the name "checkra1n" - this can take a couple seconds after the first start, just wait a while and then search your apps.

![checkra1n Options]({{ site.url }}/assets/article2/14checkra1nInstalled.png){: .center-image}

20. Open your newly installed checkra1n app. This verifies a successful installation. You can now proceed and install the Cydia store to download applications like OpenSSH, UNIX tools, SSLKillSwitch usw.

![checkra1n Options]({{ site.url }}/assets/article2/15checkra1nAppOpened.png){: .center-image}  

Congratulations to your jailbroken iDevice!

---
Thank you very much for reading this article and feel free to tell me if you agree or disagree. Subscribe and share!
If you want to read my opinion about hacking iOS apps, visit my first article ["Hacking Mobile Apps - easier done than said!"][easierDoneThanSaid].

All the best,  
Florian

[corellium]: https://www.corellium.com/?ref=himalayas.app
[checkra1n]: https://checkra.in/
[ubuntu]: https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#1-overview
[WSL]: https://docs.microsoft.com/en-us/windows/wsl/about
[easierDoneThanSaid]: http://www.florianwagner.me/mobile/app/hacking/2021/10/15/iOS-App-Penetration-Testing.html
[cc]: https://creativecommons.org/licenses/by-nc-nd/4.0/


<style>
.center-image
{
    margin: 0 auto;
    display: block;
}
</style>/Users/florian/Documents/work/website/florianwagnerdotme.github.io/assets 
