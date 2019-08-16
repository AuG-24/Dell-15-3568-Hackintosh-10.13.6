# Dell-15-3568-Hackintosh-10.13.6
Guide to install macOS 10.13.6 on Dell 15 3568 laptop
Hello Everyone !

This is a guide on how to install macOS High Sierra 10.13.6 on Dell 15 3568 laptop without using mac computer..

This process is completed without using a mac computer . But will require Windows ..

No specific windows required... Windows 7/8/8.1/10 .. all will do .. 

So Lets start...

Laptop Specifications :-

Processor :- i3 6006u 2.0 Ghz
Ram :- 4 GB DDR4 
Graphics :- Integrated Intel HD Graphics 520
1 USB 2 port ; 2 USB 3 port
HDMI 
CD Drive
SD Card Reader

Wifi :- Qualcomm Artheros QCA 9377 (Wont Work .. You Will need to buy a USB WiFi adaptor .. I prefer TP Link TP-WN725N ..Its cheap .. and is supported on High Sierra..)
Bluetooth :- Works out of the box in High Sierra..


Step 1:- Visit this link -----> https://drive.google.com/open?id=1x0XjedNrD5eaK0BCxqhy1AyxjwfrClXg

Step 2:- Download OSX_10.13.6_Installer.hfs 

Step 3:- Download Clover.img

Step 4:- Download CloverBootDiskCreater.exe

Step 5:- Insert your pendrive . Recommended capacity 8 GB +

Step 6:- Double click on CloverBootDiskCreater.exe

Step 7:- In the first box .. select your Clover.img which you downloaded previously 

Step 8:- In the second box.. select your OSX_10.13.6_Installer.hfs which you downloaded previously

Step 9:- In target disk , select your USB

Step 10:- Click OK.

Step 11:- After you get a dialog box which says "Done" , Close CloverBootDiskCreater

Step 12:- At this point you will get a dialog box which says that Windows cannot read your usb so you need to format it .. Dont Worry.. 
          Just close that window .. This is happening because now your pendrive is essentially a macOS Recovery drive ..
         
Step 13:- You will have two partitions .. Click on E drive ... not F (Names might be different .. just click on that drive which doesnt give you a "You need to format"error)

Step 14:- Delete EFI Folder ..

Step 15:- Download EFI Folder from this post ..

Step 16:- Paste this in the place of that EFI Folder..

Step 17:- Congrats ... you are half way through .. 

Step 18:- Now there are some settings which you need to disbale in your bios .. keep pressing F2 when dell logo comes.. 

Step 19:- Disable Virtualisation support .. Save and reboot

Step 20:- When Dell logo comes .. keep pressing F12 .. Select to boot from your USB ..

Step 21:- Now you need to refer some youtube guide on how to proceed with standard macOS install .. its pretty simple ..I have listed some steps here...

Step 22:-First click on Disk Utility .. Go to Top left ..click 3 horizontal lines.. Show All devices .. Select your hard drive .. click on Erase.. Name it anything .. make sure partition scheme is set to GUID..

Step 23:- Then close Disk Utility.. Click on Install macOS ..

Step 24:- I highly recommend you to watch a hackintosh guide on how to install macOS .. its standard ..

Post Installation :- (when you are in your High Sierra for first time..)

Step 25 :- Download clover efi bootloader from sourceforge .. 

Step 26:- Go watch a guide on how to install it properly... 

Step 27:- Open up CLOVER folder in your pendrive .. and EFI folder ..(If you cant see EFI folder .. click on finder .. go to top left.. click again on finder .. preferences...tick Hard Disks..)

Step 28:- Delete EFI folder from EFI partition.. Copy EFI folder from your USB to EFI partition..

Step 29:- Congrats ... if you are on this step.. you are brilliant ..Remove your pendrive.. Now restart your mac...

Audio :-

Step 30:- Download KextBeast from tony's website .. (you need to create an account to download it..)

Step 31:- Download AppleALC.kext and Lilu.kext .. Place them on Desktop.. Right click KextBeast .. Open .. Install to Library/Extensions ..

Step 32:- Restart .. Hope your Audio works now.. From Inernal Speakers that is .. From headphone jack .. It will require more work..

Step 33:- Click https://www.tonymacx86.com/attachments/alcplugfix-zip.284678/

Step 34:- Right click on install command ... click open ..

Step 35:- Open terminal .. type this...----> hda-verb 0x19 0x707 0x20

Step 36:- Press Enter..

Step 37:- Audio is done ... Hopefully ...

Brightness fix:-

Step 38:- Download Clover Configurator..Open it .. Go to Mount EFI .. Click on mount partition..

Step 39:- Download this--->https://bitbucket.org/RehabMan/applebacklightfixup/downloads/RehabMan-BacklightFixup-2018-1013.zip

Step 40:- Rename the folder .. Rename it RehabMan-BacklightFixup 

Step 41:- Open Terminal.. type this ---> sudo cp -R ~/Downloads/RehabMan-BacklightFixup/Release/AppleBacklightFixup.kext /Library/Extensions

Step 42:- click enter.. 

Step 43:- type this in terminal --> sudo kextcache -i /

Step 44:- Hit Enter...

Step 45:- Congrats on you new Macbook Pro ...

What Works :- Everything except WiFi and SD Card Reader .. 

You can get Internet Working using USB tethering ... Refer this on internet ... HornDis Package ..

Download Android File Transfer to be able to transfer files from Android phone to your Mac...

All Apple Services work out of the box.. iCloud..iMessage ..App Store ..

DO NOT FUCKING UPDATE YOUR MAC ... Mostly it breaks the system .. Otherwise your wish .. You are already on a very secure operating system ..

If you liked this tutorial .. Consider Donating .. Scan the Attached QR Code from PayTM..





