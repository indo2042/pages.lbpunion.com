# UnionRemotePatcher Guide
This is a quick guide on how to patch your copy of LittleBigPlanet on PlayStation 3 using the UnionRemotePatcher software.

## Downloading Files
To get started, you'll need to download a copy of UnionRemotePatcher for your platform. Right now, we offer builds for both Windows and Linux. You can either clone the code from https://www.github.com/LBPUnion/UnionRemotePatcher or download our binaries.

Quick Download;

[UnionRemotePatcher-Windows.zip](https://lbpunion.github.io/UnionRemotePatcher-Windows.zip) (x64)

[UnionRemotePatcher-Linux.zip](https://lbpunion.github.io/UnionRemotePatcher-Linux.zip) (x64)

Alongside the UnionRemotePatcher Application, you will also need to download the .NET 6.0 Desktop Runtime if you're on Windows, or the .NET 6.0 Runtime if you're on Linux, which can be obtained from [this page](https://dotnet.microsoft.com/en-us/download/dotnet/6.0), or, if you want direct links (may be slightly out of date);

[.NET 6.0.3 Desktop Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-6.0.3-windows-x64-installer) (Windows x64)

[.NET 6.0.3 Runtime](https://docs.microsoft.com/en-us/dotnet/core/install/linux?WT.mc_id=dotnet-35129-website) (Linux x64)

## Running the Patcher
Install the .NET Runtime appropriate for your platform, and then unzip UnionRemotePatcher. You'll need to find the executable for your platform - if you're running on Windows, look for the file ``UnionRemotePatcher.Wpf.exe``, and if you're on Linux, run ``UnionRemotePatcher.Gtk``. The main UI should open.

## Preparing your Console
In order for UnionRemotePatcher to work properly, you will need a PlayStation 3 console with either CFW or PS3HEN, and a way to host an FTP server for your console. We strongly recommend installing [WebMan-MOD](https://github.com/aldostools/webMAN-MOD/releases) on your system as it will provide UnionRemotePatcher with everything it needs in order for you to patch both PSN/Digital and Disc copies.

*Please note: if you have PS3HEN, you will need to make sure to start it between every reboot as you follow the steps of this guide, and you will need to start HEN every time you want to play a patched copy of LittleBigPlanet.*

If you are patching a PSN/Digital copy of LittleBigPlanet, you will have to complete one other quick step within WebMan-MOD to enable a required feature. To do so, navigate to your PS3's IP address inside a web brower, and navigate to the Setup screen using the Setup button;

![WebMan-MOD Home Screenshot](https://lbpunion.github.io/WebManSetup1.png)

##### If you're not sure how to access this page, open your XMB and enable HEN if neccessary, then hold the START and SELECT buttons together on your controller to get a notification listing out some information about your console;

![XMB Screenshot](https://lbpunion.github.io/InfoNotification.png)

##### As you can see in the top right corner, the IP address of my PS3 console is 192.168.0.235 - which is what I entered as the URL in Firefox.

Within the Setup tab, expand the section ``XMB/In-Game PAD Shortcuts``, enable ``PS3MAPI``, and ``Save``;

![WebMan-MOD Setup Screenshot](https://lbpunion.github.io/WebManSetup2.png)

## Getting your title's Game ID

In order for UnionRemotePatcher to find the game you're attempting to patch, you need to provide it with a Game ID. This is the name of a folder where the game files are installed on your PS3.

If you have a disc copy, the easiest way to find this is to look at the spine of the case - the Game ID can be found next to the ESRB rating symbols on US copies of LittleBigPlanet. In this case, LittleBigPlanet 2 Special Edition's Game ID, according to the artwork, is BCUS98372;

![Game Cover](https://lbpunion.github.io/IMG_20220319_105828.jpg)

But this isn't always a perfect method, either. For one reason or another, the ID on your case might not match the ID on the data of your disc, and of course, if you have a digital copy, this isn't going to be helpful. For these reasons, we recommend that you also use WebMan-MOD to check the file structure of your PS3's hard drive, and determine the Game ID there.

Navigate to the Files page, enter ``/dev_hdd0/`` and go into the ``game`` folder (not ``GAMES``). Here, you'll see a bunch of different Game IDs for different games, DLC installations, and save data on your system;

![WebMan-MOD Games folder](https://lbpunion.github.io/WebManSetup3.png)

Hover over some of the folders with your mouse. In the screenshot, as I hovered over NPUA81116, you can see that the LittleBigPlanet 3 logo was displayed, meaning this is likely a LittleBigPlanet 3 game folder.

In order to verify that this is the actual game folder, and not a DLC folder for instance, we can go inside the folder, and then entering the ``USRDIR`` folder if it exists;

![WebMan-MOD USRDIR folder lbp3](https://lbpunion.github.io/WebManSetup4.png)

As you can see, the ``EBOOT.BIN`` file, which UnionRemotePatcher patches, is located in this folder. **If there is no EBOOT.BIN, or no USRDIR folder, it's not the correct folder! If you didn't see a LittleBigPlanet logo of some kind when navigating into this folder, it's not the correct folder!**

## Patching

Using all the information that we have gathered throughout the process - our PS3's local IP address, and the Game ID of the game you wish to patch - you can go to UnionRemotePatcher and enter your information.

![UnionRemotePatcher Screenshot](https://lbpunion.github.io/UnionRemotePatcherScreenshot.png)

Fill out the boxes as neccessary. Keep in mind that for LittleBigPlanet 3, the server URL must start with ``https``. For other versions, use ``http``.

The FTP authentication information should stay the way it is unless you know that you changed your FTP username and password.

Ensure that PS3HEN is running if neccessary, and click Patch. Have fun!
