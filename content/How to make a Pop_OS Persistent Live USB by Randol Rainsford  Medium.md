---
{"dg-publish":true,"permalink":"/how-to-make-a-pop-os-persistent-live-usb-by-randol-rainsford-medium/"}
---

# How to make a Pop!_OS Persistent Live USB | by Randol Rainsford | Medium

Created Time: May 22, 2021 1:06 AM
Database: Inbox Database
Last Edited Time: June 9, 2021 9:18 PM
Status: Archived
URL: https://medium.com/@randol_rainsford/how-to-make-a-pop-os-persistent-live-usb-f96e776dccc

![https://miro.medium.com/max/1200/1*QACfPk4SYqLfFDhwa8GDlw.png](https://miro.medium.com/max/1200/1*QACfPk4SYqLfFDhwa8GDlw.png)

---

This article will help you build a Pop!_OS Live USB with Persistence enabled, which doesn’t happen without a little manual help.

This article assumes you are running Ubuntu, or an Ubuntu derivative.

> Here we will install mkusb, and write our ISO to our USB.
> 

First, we’ll need to install some packages, and download Pop OS. I’m using 19.04, but this should work with other versions. [Download Pop OS](https://system76.com/pop).

Install [mkusb](https://help.ubuntu.com/community/mkusb) (and gparted if you don’t have that already):

```
sudo add-apt-repository ppa:mkusb/ppa
sudo apt update
sudo apt install mkusb mkusb-nox usb-pack-efi gparted
```

In Terminal, run `guidus` to get started. We’ll select Install

![How to mak/13l6zUkX94kzaVTQhqGpy3A.png](/img/user/assets/How%20to%20mak/13l6zUkX94kzaVTQhqGpy3A.png)

Install

Select **Persistence**, then choose your ISO and your USB device.

For Persistence settings, we’ll **Use Defaults**.

![How to mak/1u03tYZAQ8x7Ou0lZaacDSw.png](/img/user/assets/How%20to%20mak/1u03tYZAQ8x7Ou0lZaacDSw.png)

Use Defaults

Choose your persistence size, then **Go**.

Atthis point, you’ll see a few warnings. That’s okay. Just click OK to those warnings.

When it asks if you want to use **grub.img**, answer **YES**.

Once completed, you can close mkusb.

![How to mak/1AOXu67SKG2OiK5hI2Hy05A.png](/img/user/assets/How%20to%20mak/1AOXu67SKG2OiK5hI2Hy05A.png)

Easy Day

Here we will make a few manual changes to get persistence working.

Now open **gparted**, and find our drive that we’ve just installed to. In my example, my drive is mounted at **/dev/sdb**, but yours might be a different letter. I’ll use sdb for this guide.

We first need to rename **/dev/sdb5** from **casper_pop-os_19** to simply be **casper-rw**. Right click it, and choose **Label File System**.

From This:

![How to mak/1hNzRi6UEmDycoNzQn-LO8A.png](/img/user/assets/How%20to%20mak/1hNzRi6UEmDycoNzQn-LO8A.png)

Wrong!

To This:

![How to mak/17Wrx20kQfg0CDqRB3zw1MQ.png](/img/user/assets/How%20to%20mak/17Wrx20kQfg0CDqRB3zw1MQ.png)

Yeah, looks right.

Next, take note of where your **usbboot** partition is. Mine is at **/dev/sdb3**.

In terminal, we’ll mount that to a folder. Remember to change the letter **b** below in sd**X**3 to match your system, if needed. After we mount the folder, we’ll edit **grub.cfg**. I’ll use **gedit** to edit this file, but any text editor should work (like **nano**).

```
mkdir boot
sudo mount /dev/sdb3 boot
sudo gedit boot/boot/grub/grub.cfg
```

In this guide, we will only change the first entry, but you can do what you want with the others while you’re here.

**Make Persistence Work:**

The first entry, on my system, looks like this- yours will be similar.

```
menuentry "Pop-os_19.04_amd64_intel_10.iso - persistent live" {
 search --set=root --fs-uuid 2019-08-06-15-10-16-00
 linux ($root)/casper_pop-os_19.04_amd64_intel_debug_34/vmlinuz.efi boot=casper_pop-os_19.04_amd64_intel_debug_34 quiet splash persistent --
 initrd ($root)/casper_pop-os_19.04_amd64_intel_debug_34/initrd.gz
}
```

I’m going to change it, and bold the changes below. Note that you might have different build numbers (intel_debug_34 in mine) and that’s okay. Leave those as they are. Also notice that some lines are modified, like the **boot=casper [space]** line. While we are here, I’m going to make the title a little prettier too, naming it simply **Pop OS 19.04**.

We are changing the line that says **boot=casper_pop-os_19.04_amd64_intel_debug_34** to now read **boot=casper live-media-path=casper_pop-os_19.04_amd64_intel_debug_34**

We are also adding **hostname=pop-os** and **username=pop-os.**

Here’s my new first entry in the file:

```
menuentry "Pop OS 19.04" {
 search --set=root --fs-uuid 2019-08-06-15-10-16-00
 linux ($root)/casper_pop-os_19.04_amd64_intel_debug_34/vmlinuz.efiboot=casper live-media-path=/casper_pop-os_19.04_amd64_intel_debug_34 quiet splash persistenthostname=pop-os username=pop-os--
 initrd ($root)/casper_pop-os_19.04_amd64_intel_debug_34/initrd.gz
}
```

Save and close the file.

Umount the folder, and reboot into your new system.

```
sudo umount boot
```

This will pop up every time you boot, even though it’s persistent. We don’t need this in persistence mode, and if we want to do a full install, it will still be available through Live mode.

![How to mak/16sLkyfz2laOkABdd5j2neA.png](/img/user/assets/How%20to%20mak/16sLkyfz2laOkABdd5j2neA.png)

We will close and uninstall this.

Work through the steps, then choose ‘Try Pop Live Mode’

Now open terminal and uninstall the installer.

```
sudo apt purge pop-installer*
```

Now make a simple change, like the background, and reboot to verify that your system is now persistent.