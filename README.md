![Wii Shoplift Channel](http://transfer.archivete.am/9Qu6m/wiishop.png)

Before we begin, I will say that I'm not responsible for what you do with this, this tool is a grey area.

This tool is intended to provide a way to download games from the Wii Shop directly onto your Wii, even after shutdown.

After the disaster that was Rii Shop where I was hit with a accusation that I used it to dox people, which was false (and I got harassment and some scary stuff happened as a result and it devastated me how the community reacted), people have tried making a Wii Shop revival themselves, however I found that all of them have failed to make a working shop revival. None of them worked...until now.

How does this work? You install a patched IOS56 for the Wii Shop Channel, install a ton of tickets, and then use this homebrew app to select what game you want from the Wii Shop Channel, and it launches the shop then navigates to the download page in the Wii Shop Channel.

Here are the instructions to set this up.

1. Making a NAND backup is recommended prior to trying this.
2. Download the zip and extract it to your SD. This will take a little bit, because thousands of WAD files containing tickets are in the zip.
3. Install the corresponding IOS56 in the wad folder with your favorite WAD manager. Make sure you select the right one for your console.
4. Download and install [WiiXplorer](http://wiibrew.org/wiki/WiiXplorer).
5. Go to Start > Settings > Boot Settings > Enable NAND Write Access. Press Yes, then Accept, then press Back until you get back to the main menu.
6. Open the ticket folder. Wait a couple minutes. Hold down 1 on one of the files, then select Properties. If the total file size is 1.69 MB you can continue. Otherwise, you will have to wait for the other files to load.
7. Hold down 1 on one of the files again, then press the Plus Button on your Wii Remote, then press Copy. Then navigate to NAND -> ticket -> 00010001. Press the Plus Button again, and then press Paste. Wait until this process finishes. If you get a dialog asking if you want to replace files, select No to All.
8. Open Wii Shoplifting Channel and select the game you want to download. The Wii Shop Channel will download the game and it will appear on your Wii Menu. If you get error 209601 during download you can ignore it. Also, if you turn on support to download directly to the SD, it might not work if the file size is large
9. You can now enjoy the game
