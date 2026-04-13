# Linux on MacBook Pro 14,2

These instructions are for this specific MacBook model: **Macbook Pro 14,2**.

- Linux distribution: Kubuntu 25.10
- Kernel: Linux 6.17.0-20-generic
- Desktop environment: KDE Plasma 6.4.5

This is my documentation of some configurations and tweaks I have made on my MacBook Pro 14,2 after installing Kubuntu 25.10. I am dual-booting with macOS Ventura. This guide is mainly made so that I can redo my setup when I reinstall or upgrade Linux. Note that most of the terminal commands need to be run as root.

There are instructions to:
- [Make the WiFi connection working](WiFi.md)
- [Install Audio Drivers to enable the internal audio](AudioDrivers.md)
- [Enable the firewall and open ports for LocalSend](Firewall)
- [Install Flatpak and enable the Flathub repository](FlatpakFlathub.md)
- [Configure the Mac startup manager with a custom label and icon, as well as enabling the disk selector automatically on boot.](StartupManager.md)

**Sources:**
- [https://askubuntu.com/questions/55868/installing-broadcom-wireless-drivers](https://askubuntu.com/questions/55868/installing-broadcom-wireless-drivers)
- [https://github.com/davidjo/snd_hda_macbookpro](https://github.com/davidjo/snd_hda_macbookpro)
- [https://wiki.t2linux.org/guides/startup-manager/](https://wiki.t2linux.org/guides/startup-manager/)
- [https://osxdaily.com/2021/02/26/make-intel-mac-boot-startup-manager/](https://osxdaily.com/2021/02/26/make-intel-mac-boot-startup-manager/)
- [https://flatpak.org/setup/](https://flatpak.org/setup/)
- [https://github.com/localsend/localsend/issues/1230](https://github.com/localsend/localsend/issues/1230)
- [https://help.ubuntu.com/community/UFW](https://help.ubuntu.com/community/UFW)