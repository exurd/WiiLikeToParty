![Wii Like To Party](https://github.com/exurd/WiiLikeToParty/blob/main/assets/logo.png)

This is a fork of larsenv's [WiiShopliftChannel](https://github.com/larsenv/WiiShopliftChannel). I aim it to be simple, easy to use and understandable.

This program is similar to PKGj/PKGi; the game is downloaded via the official CDN network, with a secondary file (a ticket) to help. Using a patched IOS56, the program can permit the Wii Shop Channel to install titles.

When you select a title, the program automatically searches through a local database and installs the exact ticket needed. **No other tickets are installed. No tickets need to be manually installed for it to work.**

>[!NOTE]
> Commits that I have made for this forked project is licensed under The Unlicense. For more information, read the UNLICENSE file.

# Instructions

## Before anything...
[Backup.](https://wii.hacks.guide/bootmii.html) [Your.](https://wii.hacks.guide/bootmii.html) [NAND.](https://wii.hacks.guide/bootmii.html) If backed up correctly, you will be able to easily revert any changes made by the instructions or program via BootMii.

## Preparation
Download the [latest release](https://github.com/exurd/WiiLikeToParty/releases) and extract the zip file.

There will be two folders: `apps` and `wad`. Each of these files are important for the program to run.

- The `apps` folder contains the program, called `WiiLikeToParty`.

- The `wad` folder will contain two patched IOS56 files and a forwarder. One patch is for Wii and the other is for the Wii U<!-- (or to nerds vWii)-->. Make sure to use the correct one for your console!

With your SD Card mounted, and at root level (`D:\`, not `D:\folder\`), follow through these steps.

1. Copy the `WiiLikeToParty` folder into the root `apps` folder on your SD card.
2. Copy the correct `.wad` for your system to the root wad folder of your SD card.

Eject the SD card and insert into your console.

## Installing the WAD

Open the Homebrew Launcher and select the WAD manager of your choice. Install the patched WAD to your NAND.

> [!WARNING]
> If you are finished with the program or have second thoughts after installing the IOS, **DO NOT ATTEMPT TO UNINSTALL THE IOS WAD!** If you uninstall the IOS, the WAD manager will do as you ask and remove the IOS *entirely*, turning your console into a brick unless recovered via BootMii. Instead, download a fresh IOS58 from NUS (or ModMii) and install that.

## Running

Open the Homebrew Launcher of your choice and select the `WiiLikeToParty` tile. You will be greeted with some warnings. Press A once you have read them.

A list of games will appear. Using the D-Pad, you can move the cursor up and down. Skip pages with left and right. Select where you want to install the title (SD card or NAND) with 1.

Once you have found a game you want to download, press A. The program will then attempt to install the selected game's ticket **(and only the game's ticket)**.

If the ticket successfully installed, you can select the option to open the Wii Shop Channel. Otherwise, take note of the error (press B to exit the install screen).

If you do not want to install anything, press the Home Button and the program will exit.

When you open the Wii Shop Channel, select Yes to download the title. If you lose the download screen, you must open the `WiiLikeToParty` program and choose your title to reaccess the screen.

# Compiling

You will need [devkitPro](https://devkitpro.org/) installed with the Wii compiler. Windows is the easiest way to run the SDK.

In a terminal, clone the repository:
```sh
git clone --recurse-submodules -j8 https://github.com/exurd/WiiLikeToParty.git
```

> [!IMPORTANT]
> If you only do a `git clone`, it will not retrieve everything needed and the code will not compile. If you have already cloned the repo, running `git submodule update --init` inside the directory will get the required dependencies.

Next, `cd` into the cloned repository and run `make`. When successfully compiled, you will have a .elf and .dol file.

If you want to create a release zip file, run the script for your system (`build.bat`,`build.sh`).


# Wii Shop Error Codes

- 204036 - IOS56 has not been patched yet. Dolphin currently errors with this, even after installing the patched IOS.
- 204050 - The ticket was not installed correctly.
- 205626 - The Wii has been region changed. Change your region to its prior setting, or delete your Wii Shop account to create an account based on the new region.
- 209601 - This error can happen when taking too long to choose an option.

<!-- Some titles are too large for the SD card, which can error out. -->

# Credits
Thank you rxi for [microtar](https://github.com/rxi/microtar), larsenv for the original repository, [WiiShopliftChannel](https://github.com/larsenv/WiiShopliftChannel), and to everyone involved with [yawmME](https://github.com/modmii/YAWM-ModMii-Edition): I would've not gotten this far without your amazing efforts in Wii homebrewing!
