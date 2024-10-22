+++
title = 'Access Android emulator savefiles'
date = 2024-10-21T14:25:56+03:00
tags = ['emulation', 'android']
draft = false
+++

Accessing files on the latest versions of Android can be a pain, especially as Android decided to lock users out of the `Android/data` folder. As such, it's also a pain to access savefiles from emulation (e.g. Lemuroid game files).

This guide will walk you through how to access these files and go around Android's restrictions.

{{< toc >}}

## Workaround for restrictions

To access the files, I found that an app called [EX File Manager](https://play.google.com/store/apps/details?id=com.ace.ex.file.manager) was really helpful in accessing the `Android/data` folder.

*NOTE: I'm not quite sure how safe this software is. It has ads and is definitely not FOSS. However, I can vouch for its effectiveness.*

For the rest of this guide, I will assume that you are using this app.

## Getting the files

Now that we have a working file manager, we can go into the required folders.

### The Android/data folder

From the homescreen of EX File Manager click on the hamburger menu icon on the upper-left. This should reveal a menu.

Under **Storage**, click on **Internal Storage**.

This should lead you to a screen with all your folders under `/storage/emulated/0`. Think of this as your home folder.

Find and access the folder named **Android**, then **data**. You're in!

### Finding the application's folder

You might notice that `/storage/emulated/0/Android/data` has *tons* of folders. Each folder is managed by one of your applications.

From what I figure, the folders are named by the domain name of the app's publisher. For instance, we have `org.fdroid.fdroid` for F-droid, and `md.obsidian` for Obsidian.

Let's say you're using **Lemuroid** as your emulator. From here on, I'll assume that you're using this.

For me, Lemuroid is all the way down, as `com.swordfish.lemuroid`. It's a lot to scan through, but EX File Manager shows a thumbnail of the application for each folder.

### Getting the savefile

Under `com.swordfish.lemuroid/files`, there are four folders:

- `roms`
- `saves`
- `state-previews`
- `states`

The file structure may differ per emulator, but usually you'll find a folder containing similarly-named folders.

Navigate into the `saves` folder.

Here, you should see a bunch of files in the format `romName.dsv`. The file extension (e.g. `.dsv` or `.sav`) differs between emulators.

*NOTE: saves are different from save states! Save your games in-game in order to generate the actual savefiles.*

Long press on the file you need to select it, then on the lower-left click on **Copy**.

## That's it!

**Paste** the file into the desired folder, and there you have your savefile!
