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
Install the .NET Runtime appropriate for your platform, and then unzip UnionRemotePatcher. You'll need to find the executable for your platform - if you're running on Windows, look for the file ``UnionRemotePatcher.Wpf.exe``, and if you're on Linux, run ``UnionRemotePatcher.Gtk``.

## Preparing your Console
In order for UnionRemotePatcher to work properly, you will need a PlayStation 3 console with either CFW or PS3HEN, and a way to host an FTP server for your console. We strongly recommend installing [WebMan-MOD](https://github.com/aldostools/webMAN-MOD/releases) on your system as it will provide UnionRemotePatcher with everything it needs in order for you to patch both PSN/Digital and Disc copies.

If you are patching a PSN/Digital copy of LittleBigPlanet, you will have to complete one other quick step within WebMan-MOD to enable a required feature. To do so, navigate to your PS3's IP address inside a web brower;
