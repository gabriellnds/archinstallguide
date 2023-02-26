[![Arch Explanation](https://img.shields.io/badge/Arch_Explanation-4B275F?style=for-the-badge&logo=elixir&logoColor=white)](https://github.com/gabriellnds/archinstallguide)

Arch Linux is the operating system of choice for many packages around the world, and there are many communities that provide help and documents in many different languages.

So remember if you have problems you are not alone:

[# International Communities](https://wiki.archlinux.org/title/international_communities)

##

**`This document is a guide to installing Arch Linux using archinstall.`**

Arch Linux does not support Secure Boot and you need to disable it in the UEFI interface settings or your BIOS-Legacy. Once installed, you can configure your Arch Linux without problems.

When it starts for the first time choose the first option! Then the base system will be loaded.

![Arch Linux Install Medium](https://user-images.githubusercontent.com/126100626/220797958-dd6399bc-8bdb-4f29-b3b7-5feec7b27339.png)

![NetWork](https://img.shields.io/badge/NetWork-05@0?style=for-the-badge&logo=rss&logoColor=white)

However, if you are a laptop user you will find that it will not be possible to continue due to the lack of WIFI connection. It is necessary to use the Iwctl command, which will enable the use of the network:

```
[iwd]# iwctl
```
Which will show the name of devices in local network.

```
[iwd]# device list
```
With the name of your device in hand, you just have to be aware of the name of the network you want to use!
```
[iwd]# station YOURDEVICE connect YOURSSID
```
Putting the network password, just exit the iwd.
```
[iwd]# exit
```
#

![ArchInstall](https://img.shields.io/badge/ArchInstall-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)

**`And archinstall Options.`**

### Remember that:

- To navigate between options, use the up and down arrows;
- To open the menu with the options and to confirm, click Enter;
- In fields with many items, click on “/” (without quotation marks) to search (note that the default keyboard is in English).

With the archinstall command, the option of being able to configure the entire system will be enabled.

```
$ archinstall
```

![ArchInstall](https://user-images.githubusercontent.com/126100626/220801043-96aed4a8-5d55-46ee-a4d6-5cad2559c54a.png)
**`And one thing to remember is that many of these options are user dependent, so they shouldn't be used as the only way to configure.`**

### Initial Options

- Archinstall language
- keyboard layout
- mirror region
- localization language
- location encoding

Therefore, all the above options must be chosen by the end user.

### Storage Units and Unit Layout:

If you want to use the entire disk to install Arch Linux, just choose “Erase all selected disks and use a better performing default partition scheme”.

**I recommend BTRFS as it has many benefits and great performance for any machine:**

![BTRFS](https://user-images.githubusercontent.com/126100626/220807777-aabb8db3-3229-43b5-98a1-197d2330721f.png)
### Moving on to other options

- encryption password

- launcher

- swap

- Computer name (hostname)

### Root password:

Choose (and confirm) the password for the root user; if you leave the password blank, the root user will be disabled and you will need to use sudo to escalate the privileges of at least one of the users.

Anyway, I recommend that you set (and write it down!) the root password so you never get “locked” out of the system. The system indicates password strength, but does not block the use of weak passwords;

- User Account

### Profile:

This being the most important part, it will determine your GUI.

it's a kind of user interface that allows interaction with electronic equipment through graphic icons and other visual elements.

**`These are the easiest for daily use.`**

- Budgie
- Cinnamon
- Deepin
- GNOME
- KDE
- LXQt
- MATE
- XFCE4

Next, you can choose the proprietary video drivers for your system, or use the open source (default) drivers. Not all proprietary drivers may be available, in which case you can install the drivers later using the manufacturer's instructions.

- Audio
- Kernels

### Additional Packages:

I suggest that you install at least one browser, so that in the future you don't have to configure so many options. (firefox for example)

```
$ firefox
```

![Additional Packages](https://user-images.githubusercontent.com/126100626/220894737-214e0696-ee80-481a-ab6f-312f3a965c4d.png)
### Network Configuration:

it is something that depends on the graphical environment that was chosen earlier.

**`I recommend`**

Use NetworkManager (needed for graphically configuring the internet in GNOME, KDE and other supported graphical environments)

- Time Zone
- Automatic Time Synchronization (NTP)

### Additional Repositories:

Choose if you want to enable multilib repositories (necessary for developers, to use Steam and many games)

### End of Installation:

Now you can start the installation by clicking “Install”. The system will show the chosen settings on the screen, followed by the installation of the files.

The process may take some time depending on your connection speed, kernels and chosen graphical environments. Once the installation is complete, Archinstall asks if you want to do some post-installation configuration (via chroot), otherwise choose “no” and green text will appear saying it's safe to reboot.
```
$ reboot
```

**When it restarts, it will boot into Arch Linux and can be used without any problems.**

![GitHub](https://img.shields.io/badge/By_Gabriel-100000?style=for-the-badge&logo=github&logoColor=white)
