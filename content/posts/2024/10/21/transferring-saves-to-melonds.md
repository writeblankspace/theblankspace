+++
title = 'Transferring saves to MelonDS'
date = 2024-10-21T14:56:06+03:00
tags = ['emulation', 'melonDS']
draft = false
+++

For some, getting started with MelonDS could get confusing. Perhaps you're using it for the same reasons as me: to use the multiplayer feature.

Here is a step-by-step guide on how to open your game on MelonDS for desktop.

{{< toc >}}

## Prerequisites

You'll need:

- The [MelonDS desktop app](https://melonds.org/download/)
- Your ROM file (usually a `.zip`)
- Your savefile (file extension depends on emulator and core)

If you don't have your savefile, try checking out the article on [accessing Android emulator savefiles](../access-android-emulator-savefiles/).

## Compatibility

Savefiles from other cores (such as DeSmuMe) are mildly incompatible with MelonDS.

If you're not sure which one you're using, check your emulator or your savefile's file extension. If the file ends in `.sav`, you're good to go. If not, you might want to [convert between the file types](https://www.save-editor.com/tools/wse_ds_save_converter_for_emulator_desmume_dsv.html). 

No, simply renaming the file does *not* work.

## Getting started

Launch up MelonDS.

You'll be met with a blank, black screen. Don't worry; nothing's broken.

Your OS should have a native menu for the application with the following items:

- File
- System
- Config

On Windows, the menu should be accessible within the window. On MacOS, look to the top taskbar. On Linux, you're on your own — you're probably smart enough to know where to look for this.

Follow the following steps:

1. Navigate to **File > Open ROM**
2. Select your ROM file
3. The game should start up. Go to **File > Import savefile**.
4. Select your savefile

The game should restart and, if all went well, you can access everything from your save. Yipee!

## Final words

I have a couple of articles for emulation, which you can find here: [#emulation](/tags/emulation). This includes articles on accessing your savefiles from Android as well as how to use Multiplayer on MelonDS for desktop.

Hope these help! Cheers!
