<figure class="gpi">
<link href="https://fonts.cdnfonts.com/css/major-mono-display-2" rel="stylesheet">
                
  <figcaption>GamePi43:<br><span>Raspberry pi game console</span></figcaption>
  <style>
    @import url('https://fonts.cdnfonts.com/css/major-mono-display-2');
    .gpi {
      font-family:  'Major Mono Display', sans-serif;                                   
      font-size: 35px;
      color: yellow;
    } 
    figcaption span {
      color: turquoise;
      font-size: 30px
    }
    .image-border {
      margin: 40px;
      /* border-radius: 1vmin; */
      border: 3px solid var(--primary);
      box-shadow:
        10px 10px 0 -3px var(--background),
        10px 10px var(--green),
        20px 20px 0 -3px var(--background),
        20px 20px var(--yellow);
    }
    .image-border:hover {
      animation: shadow-wave 2.5s ease-in infinite;
    }
    @keyframes shadow-wave {
      0% {
        border: 3px solid var(--primary);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--green),
          20px 20px 0 -3px var(--background), 20px 20px var(--yellow);
      }
      20% {
        border: 3px solid var(--red);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--primary),
          20px 20px 0 -3px var(--background), 20px 20px var(--green);
      }
      40% {
        border: 3px solid var(--orange);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--red),
          20px 20px 0 -3px var(--background), 20px 20px var(--primary);
      }
      60% {
        border: 3px solid var(--yellow);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--orange),
          20px 20px 0 -3px var(--background), 20px 20px var(--red);
      }
      80% {
        border: 3px solid var(--green);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--yellow),
          20px 20px 0 -3px var(--background), 20px 20px var(--orange);
      }
      100% {
        border: 3px solid var(--primary);
        box-shadow: 10px 10px 0 -3px var(--background), 10px 10px var(--green),
          20px 20px 0 -3px var(--background), 20px 20px var(--yellow);
      }
    }
    :root {
      --primary: #22D2A0;
      --secondary: #192824;
      --background: #192824;
      --green: #1FC11B;
      --yellow: #FFD913;
      --orange: #FF9C55;
      --red: #FF5555;
    }
    @media only screen and (max-width: 600px) {
      .image-border {
        margin-left: 0;
        margin-right: 50px;
      }
    }
  </style>
</figure>

---
![header image](assets/img0.jpg)

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Devices and Supplies](#devices-and-supplies)
- [Assembly Process](#assembly-process)
  - [Before Assembling](#before-assembling)
  - [Device Assembly](#device-assembly)
- [Operating System](#operating-system)
  - [Easy Method](#easy-method)
  - [Not So Easy Method](#not-so-easy-method)
- [ROM Games](#rom-games)
  - [Using a USB Stick (or other fitting drive)](#using-a-usb-stick-or-other-fitting-drive)
  - [Wirelessly with SFTP (A More Advanced Method)](#wirelessly-with-sftp-a-more-advanced-method)
- [Pico-8 Games](#pico-8-games)
- [Customization](#customization)
  - [Default Themes](#default-themes)
  - [Non-Default Themes](#non-default-themes)
  - [Make content fit the screen](#make-content-fit-the-screen)
  - [Custom Boot Image](#custom-boot-image)
  - [Custom Boot Video](#custom-boot-video)
  - [Removing Boot Text](#removing-boot-text)
  - [Game Scraping](#game-scraping)
- [Best Practices](#best-practices)
- [Conclusion](#conclusion)

---

![Insert image here](assets/img2.jpg ":size=440vmin :class=image-border :no-zoom")

## Introduction

The GamePi43 is a retro-feel handheld gaming console that uses a Raspberry Pi as its main component.

It's fairly simple to recreate, requiring a low-to-intermediate level of technical skills for basic configuration and a high-intermediate level for customizations.

It's a great project to undertake and an amazing device to play on.

While the console's body is not ergonomic and its buttons are hard to press, it gets the job done. Although it's of lower engineering quality than consoles designed solely for gaming, its versatility and customization make it a worthwhile project even with these downsides.

Let's start with what we need for it to work:

## Devices and Supplies

Building the GamePi43 console is relatively straightforward. The necessary components include a compatible Raspberry Pi model (e.g., B+ / 2B / 3B / 3B+ / 4B). Remember to check compatibility with the [GamePi43](https://www.waveshare.com/wiki/GamePi43) device.

For my build, I used a [Raspberry Pi 4 8GB Kit from Botland](#) and a [GamePi43 from Botland](https://botland.com.pl/gaming-pi-retro-pie-konsole/17598-gamepi43-zestaw-akcesoriow-do-budowy-konsoli-dla-raspberry-pi-b-2b-3b-3b-4b-waveshare-16967-5904422327965.html?cd=1050025856&ad=55008030609&kd=&gclid=Cj0KCQjwuZGnBhD1ARIsACxbAVi_yP_z9whvMxNqS_-G67z5Up9icvYHbGoLaR1e1NCGWmEW12LuSBYaAiQnEALw_wcB).

?>**_Note:_**  
Only the Raspberry Pi is needed for this particular project. I used the full kit only because it was part of other projects. If your focus is solely on the GamePi43 console, purchasing just the Raspberry Pi is a cost-effective option.

The GamePi43 includes a screwdriver, but having your own, as well as a microfiber cloth to clean fingerprints off the screen, is recommended.

!>**_Be Aware:_**   
Batteries were NOT included in the kit I used. The console works with a charger connected directly to the power supply by cable. If you wish to have a wireless working console with a rechargeable battery, you need to buy accumulators and fit them into the place that is already inside the GamePi's body.

You may also need a clean USB stick, depending on your intended use for the console.

## Assembly Process

### Before Assembling

Prepare your workspace to avoid losing parts or damaging the board due to static shock or environmental variables. Arrange all components in an orderly fashion, and inspect them for any potential damage that might cause delays later.

!>**_Heed any warnings and precautions:_**   
These can be found on the product's website or packaging. Devices may vary, so adapt to different situations accordingly. Check for compatibility beforehand.

### Device Assembly

Assembly is fairly straightforward if you have inspected all the necessary pieces. Follow the instructions included with the GamePi43 or consult the manufacturer's website for a more detailed description.

I found [this visual YouTube tutorial](https://www.youtube.com/watch?v=HrKpUuo6OUg&t=173s) by MakerMan to be helpful.

During assembly, I encountered no significant issues. Inserting the HDMI adapter was slightly tricky but manageable. If you have a prepared SD card with the required system and games, insert it, plug in the power, and you're done! If not, further instructions on installing the [operating system](#operating-system) and [games](#pico-8-games) are provided below.

## Operating System

With the physical device ready, the next step is to install the operating system. Thankfully, Waveshare has a ready-made OS. Below, you'll find both the [easy method](#easy-method) and the [advanced method](#advanced-method).

### Easy Method

Use Waveshare's customized version of the RetroPie/Recalbox operating system, configured with input and additional tweaks found [here](https://www.waveshare.com/wiki/GamePi43).

Use imager app, like [Raspberry Pi Imager](https://www.raspberrypi.com/software/), to write the OS to the SD card. Insert it into the device, boot up, and configure settings such as timezone, WiFi, etc.

If everything goes smoothly, all that remains is installing your chosen games, whether [ROM games](#rom-games) or [Pico-8 games](#pico-8-games).

### Not So Easy Method

Install imager app (I used Raspberry Imager).

On clean SD card (or other fitting memory) burn the latest Retropie/RecallBox operating system that fits your device.

Input basic info like timezone and wifi before or after burning the image.

Insert SD drive into Gamepi's body and boot the device.

Configure carefully all that is left - mainly the input buttons.

Adjust device in settings or in terminal using `F4` key by plugging in keyboard.

And it's done, that step is harder mainly because you need to configure every part of OS manually, but it also can be done that way.

## ROM Games

Installing ROM games is incredibly simple. Below are two basic methods.

### Using a USB Stick (or other fitting drive)

Prepare a USB stick (8GB or more is recommended). Clean it and format to FAT32.

Inside create an empty directory called `retropie` (depending on the OS used that name may vary, that one worked for me byt you can also try `retropie-mount` or find other if both of them dont work).

Then update the device (skip this step if you are already on the latest OS version):

```
Main screen > RetroPie > RetroPie Setup > Basic Install
```

Enable the USB ROM Service by:

```
Main screen > RetroPie > RetroPie Setup > Configuration/tools > usbromservice - USB ROM Service > 1 Enable USB ROM Service
```

Plug your USB into the working GamePi43 device and let it run. This step is tricky because there is no indication of the process being completed unless you have a USB with a light signaling data transfer. Let it sit for 5-15 minutes, then reboot the device and plug the USB back into your computer.

If everything went right, you should have new working directories inside the USB drive. (I myself had a little issue here because for some reason my USB was not compatible with Retropie OS, and I was stuck for some time figuring out how to fix it. Luckily, I tried using another available USB device, and it worked well that time).

Now you need to find some games - it's up to you what game you want to use; for the tutorial's sake, we need the game's ROM file, and that's all.

Find the corresponding console directory within the USB drive's directories and copy the game's file into it.

Reboot the device, and you're done! You're now ready to play games on your new awesome console!

I recommend [this YouTube tutorial](https://www.youtube.com/watch?v=P1etPYvWBZU&t=373s) made by ETA PRIME if you come by any issues.

### Wirelessly with SFTP (A More Advanced Method)

For a more advanced method to transfer games, the user can utilize SFTP (SSH File Transfer Protocol).

Firstly - Enable SSH on GamePi34:
```raspi-config > Interface Options > SSH > Yes > OK > Finish```

Find devices IP address:
```RetroPie > Show IP```

Using SFTP client (e.g. FileZilla) on your device with ROM game files, connect to GamePi using it's IP and login info.

In most cases it's basic config:
```
Port: 22
```
```
Username: pi
```
```
Password: raspberry
```
When connected browse folders until you see ROM folder and transfer ROM games into according consoles.

!>**_Be Aware:_**   
It matters where you insert the game, it will work properly only when you insert it into dedicated console directory.

[In depth SSH tutorial by retropie devs.](https://retropie.org.uk/docs/SSH/)

## Pico-8 Games

You can purchase the license for Pico-8 [here](https://www.lexaloffle.com/pico-8.php#getpico8).
 

?>**Note:**    
You can often get license from buying devices in a bundle,
e.g. Picade already had pico-8 license in its box.

Once purchased, download the Raspberry Pi zip version and unzip it to your SD card (the same one with your operating system).

After that, add a folder named "pico-8" and inside it create a subfolder named "carts". Place any games you want in there.

After that, you'll have to manually launch the Pico-8. But you're good to go!

## Customization

>Now the real kicker! The best thing about this device is the ability to customize literally every part of it, I will show few ways to do that, but feel free to explore yourself, options are unlimited!

### Default Themes

One of the best options given by Retropie's devs is ability to use different console themes and even create your own!

To do so open:

```device
Retropie > raspi-config > ES Themes > Install/Update theme gallery
```

> You can view installed themes preview by going into `view theme gllery`.

Then just choose witch one you like and remember its name in bottom-left corner.

Go back to theme gallery and find `Install *theme name*` option and click it.

Now the theme is installed on your device, but not used, to do so go to devices main page and go into MAIN MENU panel:

```device
MAIN MENU > THEME SET > *choose theme by going left-right* > Back
```

Reboot device and done!

!> **_Disclaimer:_**  
Themes look differently on different screens, sometimes text is too small/big or other UI elements are off, keep that in mind while choosing one.

### Non-Default Themes

It's fairly easy, almost the same stepps as above, but we need to download custom theme or create one ourselves.

Cool one to download is [Epic Noir](https://github.com/c64-dev/es-theme-epicnoir) by Nick L (c64-dev) that has tutorial on their page on how to set it up.

!>**_Disclaimer:_**  
Not all themes look great on small screens, so keep that in mind.

Place custom theme inside `emulationstation/themes`directory by using SFTP, Terminal or other means, reboot device, and go into MAIN MENU:

```device
MAIN MENU > THEME SET > *choose theme by going left-right* > Back
```

Reboot device again and done!


### Make content fit the screen
To do so, turn off underscan:

```device
Retropie > raspi-config > display options > underscan > NO > Finish
```
### Custom Boot Image
### Custom Boot Video
### Removing Boot Text

After booting the console, you see some sort of text messages regarding booting, this doesn't concern us too much, but looks unpleasing.

Removing the text is preety straightforward:

Turn on device and go into terminal using `F4` key on plugged in keyboard.

> You can also do it with SFTP client, or other mean of accesing system files.

Then find and open the `cmdline.txt` file, I've done it by using linux command:

```terminal
sudo nano /boot/cmdline.txt
```
`sudo` - run as administrator, and accept drastic changes.

`nano` - open file using nano explorer.

`/boot/cmdline.txt` - access cmdline.txt file inside boot directry.

!> **_Be Aware:_**  
Depending on the OS used the dirctories may vary.

Inside of cmdline.txt file find `"console=tty1"` and change it to `"console=tty3"`.

When done editing press `Ctr+X` > `Y` > `Enter` to save changes.

Rebot the device.

> While you are inside of the terminal you can use command 
`reboot` to do so.

And that's all, the text shows no longer, but there is black screen for some time so i reccomend doing custom splashscreen [image](#custom-boot-image) or [video](#custom-boot-video)!

If you come by any issues ETA PRIME made a great [video explaining it](https://www.youtube.com/watch?v=KGf225Qb02I&t=65s).


### Game Scraping

## Best Practices

1. **Preparation:** Gather all the necessary tools and parts before starting, and follow the guidelines and warnings carefully.
1. **Clean Workspace:** Maintain an organized workspace to avoid losing or damaging components.
1. **Follow Instructions:** Refer to manufacturer guides and trusted tutorials.
1. **Inspect for Compatibility:** Check the compatibility of all the hardware components before purchasing.
1. **Take Your Time:** Don't rush the process; be patient with the assembly and the software installation.
1. **Backup Important Files:** If you are using an existing SD card, make sure to back up any important files before proceeding with the installation.
1. **Learn from Mistakes:** If something goes wrong, don't panic. Troubleshoot the problem, learn from it, and improve.

## Conclusion

---

Whether you're a seasoned Raspberry Pi user or a complete novice, the GamePi43 offers something for everyone. With both easy and advanced setup options, as well as numerous game choices, this console promises hours of nostalgic gaming fun.

Happy gaming!
