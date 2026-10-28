# IVSDKBanner

A tiny [IV-SDK .NET](https://github.com/ClonkAndre/IV-SDK-DotNet) script for GTA IV that tells you, once per game
launch, which **IV-SDK .NET** and **GTA IV** versions are running:

    IV-SDK .NET v1.9.1.0 is running
    GTAIV.exe v1.0.8.0

Handy for checking that IV-SDK .NET actually loaded, and for bug reports.

## Download

- [`IVSDKBanner_1.0.zip`](IVSDKBanner_1.0.zip): `IVSDKBanner.ivsdk.dll`, README and licence.
- [`IVSDKBanner_source_1.0.zip`](IVSDKBanner_source_1.0.zip): source code and `build.bat`.

## Install

Copy `IVSDKBanner.ivsdk.dll` into `GTAIV\IVSDKDotNet\scripts`. Delete it to uninstall.

Requires IV-SDK .NET by ItsClonkAndre. Works on any GTA IV version IV-SDK .NET runs on.

## How it works

- A few seconds after you're first in control, it shows a 6-second subtitle with both versions, read live from
  `IVSDKDotNetWrapper.dll` and `GTAIV.exe`.
- On GTA IV 1.2.0.59 it adds **"(Unofficial 1.2.0.59 Beta)"**, since IV-SDK .NET only runs there with the
  [unofficial fork](https://github.com/bassisthip63-ui/IV-SDK-DotNet).
- It waits until no subtitle, help message or conversation is on screen, so it never covers dialogue or mission
  text.
- It uses IV-SDK .NET's own subtitle helper (a literal string), so **none of the game's text is changed**.
- The same line goes to the IV-SDK .NET console (F4) and `IVSDKDotNet.log`.

## Build it yourself

Put the source folder inside your GTA IV folder (next to `GTAIV.exe`) and double-click `build.bat`. It uses the C#
compiler built into Windows (.NET Framework 4), compiles against your `IVSDKDotNetWrapper.dll`, and installs the
result into `IVSDKDotNet\scripts`.

## Licence and credits

MIT (see [LICENSE](LICENSE)). By bassisthip63-ui, with Claude (Anthropic).
IV-SDK .NET by ItsClonkAndre. Not affiliated with Rockstar Games or Take-Two Interactive.
