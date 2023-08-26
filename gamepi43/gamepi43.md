<figure class="gpi">
<link href="https://fonts.cdnfonts.com/css/major-mono-display-2" rel="stylesheet">
                
  <figcaption>GamePi43:<br>Raspberry pi game console</figcaption>
  <style>
    @import url('https://fonts.cdnfonts.com/css/major-mono-display-2');
    .gpi {
      font-family:  'Major Mono Display', sans-serif;                                   
      font-size: 35px;
      color: yellow;
    }
    .image{
      border-radius: 8%;
    }
  </style>
</figure>

---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Devices and Supplies](#devices-and-supplies)
- [Assembly Process](#assembly-process)
  - [Before Assembling](#before-assembling)
  - [Device Assembly](#device-assembly)
- [Operating System](#operating-system)
  - [Easy Method](#easy-method)
  - [Advanced Method](#advanced-method)
- [ROM Games](#rom-games)
  - [Using USB Stick or Compatible USB Memory](#using-usb-stick-or-compatible-usb-memory)
  - [Wirelessly with SFTP (A More Advanced Method)](#wirelessly-with-sftp-a-more-advanced-method)
- [Pico-8 Games](#pico-8-games)
  - [Best Practices:](#best-practices)
---
![Insert image here](assets/img2.jpg ':size=480vw :class=image')

## Introduction
(*Introduction content goes here.*)

## Devices and Supplies
Building the GamePi43 console is relatively straightforward. The necessary components include a compatible Raspberry Pi model (e.g., B+ / 2B / 3B / 3B+ / 4B). Remember to check compatibility with the [GamePi43](https://www.waveshare.com/wiki/GamePi43) device.

For my build, I used a [Raspberry Pi 4 8GB Kit from Botland]() and a [GamePi43 from Botland](https://botland.com.pl/gaming-pi-retro-pie-konsole/17598-gamepi43-zestaw-akcesoriow-do-budowy-konsoli-dla-raspberry-pi-b-2b-3b-3b-4b-waveshare-16967-5904422327965.html?cd=1050025856&ad=55008030609&kd=&gclid=Cj0KCQjwuZGnBhD1ARIsACxbAVi_yP_z9whvMxNqS_-G67z5Up9icvYHbGoLaR1e1NCGWmEW12LuSBYaAiQnEALw_wcB).

**_Note:_** Only the Raspberry Pi is needed for this particular project. I used the full kit only because it was part of other projects. If your focus is solely on the GamePi43 console, purchasing just the Raspberry Pi is a cost-effective option.

The GamePi43 includes a screwdriver, but having your own, as well as a microfiber cloth to clean fingerprints off the screen, is recommended.

**_Be Aware:_** Batteries were NOT included in the kit I used. The console works with a charger connected directly to the power supply by cable. If you wish to have a wireless working console with a rechargeable battery, you need to buy accumulators and fit them into the place that is already inside the GamePi's body.

You may also need a clean USB stick, depending on your intended use for the console.

## Assembly Process
### Before Assembling
Prepare your workspace to avoid losing parts or damaging the board with static shock or environmental variables. Arrange all components orderly, and inspect them for any potential damages that might cause delays later.

**_Heed any warnings and precautions:_** These can be found on the product's website or packaging. Devices may vary, so adapt to different situations accordingly.

### Device Assembly
Assembly is fairly straightforward if you have inspected all the necessary pieces. Follow the instructions included with the GamePi43 or consult the manufacturer's website for a more detailed description.

I found [this visual YouTube tutorial](https://www.youtube.com/watch?v=HrKpUuo6OUg&t=173s) by MakerMan to be helpful.

During assembly, I encountered no significant issues. Inserting the HDMI adapter was slightly tricky but manageable. If you have a prepared SD card with the required system and games, insert it, plug in the power, and you are done! If not, further instructions on installing the [operating system](#operating-system) and [games](#pico-8-games) are provided below.

## Operating System
With the physical device ready, the next step is to install the operating system. Thankfully, Waveshare has a ready-made OS. Below, you'll find both the [easy method](#easy-method) and the [advanced method](#advanced-method).

### Easy Method
Use Waveshare's customized version of the Retropie/Recalbox operating system, configured with input and additional tweaks found [here](https://www.waveshare.com/wiki/GamePi43).

Utilize an imaging application, like [Raspberry Pi Imager](https://www.raspberrypi.com/software/), to write the OS to the SD card. Insert it into the device, boot up, and configure settings such as timezone, WiFi, etc.

If everything goes smoothly, all that remains is installing your chosen games, whether [ROM games](#rom-games) or [Pico-8 games](#pico-8-games).

### Advanced Method
(*Instructions for the advanced method go here.*)

## ROM Games
Installing ROM games is incredibly straightforward. Below are two simple methods.

### Using USB Stick or Compatible USB Memory
Ready a USB stick (8GB or more is recommended).

Update the device (if you are not on the latest OS version, otherwise skip this step):
```
Main screen > Retropie > Retropie Setup > Basic install
```
Enable USB ROM Service by:
```
Main screen > Retropie > Retropie Setup > Configuration/tools > usbromservice - USB ROM Service > 1 Enable USB ROM Service
```

Now, just plug your USB into the working GamePi43 device and let it run. This step is tricky because there is no indication of the process being done if you do not have a USB with a light signaling data transfer. Let it sit for 5-15 minutes, reboot the device, unplug the USB, and plug it into your computer.

If everything went right, you should have new working directories inside the USB drive. (I myself had a little issue here because for some reason my USB was not compatible with Retropie OS, and I was stuck for some time figuring out how to fix it. Luckily, I tried using another available USB device, and it worked well that time).

Now you need to find some games - it's up to you what game you want to use; for the tutorial's sake, we need the game's ROM file, and that's all.

The game that you have has an intended console for it, so find its name inside the USB drive's directories and copy the game's file inside of it.

Now, just plug the USB back into the GamePi43 and wait until the game has been uploaded (the time that it takes varies from the size of the game and the number of games you transfer, usually taking 10-25 minutes).

I recommend [this YouTube tutorial](https://www.youtube.com/watch?v=P1etPYvWBZ

o) for an additional visual guide.

Clean and format the USB to FAT32.

Inside of the formatted USB drive create an empty directory called `retropie` (depending on the OS used that name may vary, that one worked for me byt you can also try `retropie-mount` or find other if both of them dont work)

Now we just plug our USB into working GamePi43 device and let it go running, this step ist tricky, because there is no indication of the process being done if you do not have an usb with light signaling data transfer, let it sit for 5-15 minutes, rebot device, unplug USB and plug it into your computer.

If everything went right you should have new working directories inside of the USB drive. (I myself had a litte issue here, because for some reason my USB was not compatible with Retropie OS, and i was stuck for some time figuring out how to fix it, luckily i tried using other avalible USB device and it worked well that time).

Now you need to find some games - its up to you what game you want to use, for tutorials sake we need games ROM file and thats all.

The game that you have has a intedned console for it so find its name inside of USB drive's directories and copy the games file inside of it.

Now just plug USB back into the GamePi43 and wait until the game has been uploaded (the time thet it takes varies from size of the game, and amount of games you transfer, usually it takes 10-25 min).

I recommend [this YouTube tutorial](https://www.youtube.com/watch?v=P1etPYvWBZU&t=373s) made by ETA PRIME if you come by any issues.


Reboot the device, and you are done! You are boatifully baked for playing games on your new awesome console!

### Wirelessly with SFTP (A More Advanced Method)
For a more advanced method to transfer games, the user can utilize SFTP (SSH File Transfer Protocol). Please refer to the [Waveshare Wiki page](https://www.waveshare.com/wiki/GamePi43) for more information on this process.

## Pico-8 Games
(*Instructions for Pico-8 games go here.*)

---

I hope you find this guide informative and clear! Please don't hesitate to reach out if you need additional clarification or further assistance with anything. Enjoy your Raspberry Pi GamePi43 console!

---

### Best Practices:
1. **Preparation:** Gather all the necessary tools and parts before starting, and follow the guidelines and warnings carefully.
2. **Clean Workspace:** Maintain an organized workspace to avoid losing or damaging components.
3. **Follow Instructions:** Refer to manufacturer guides and trusted tutorials.
4. **Inspect for Compatibility:** Check the compatibility of all the hardware components before purchasing.
5. **Take Your Time:** Don't rush the process; be patient with the assembly and the software installation.
6. **Backup Important Files:** If you are using an existing SD card, make sure to back up any important files before proceeding with the installation.
7. **Learn from Mistakes:** If something goes wrong, don't panic. Troubleshoot the problem, learn from it, and improve.