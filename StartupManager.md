We can configure the Mac startup disk manager with custom labels and icons, as well as enabling the manager to automatically appear at boot. Make sure to run all terminal commands as root (`sudo`).
## Labels
To set labels, first mount the EFI partition by running the following command:
```
diskutil mount disk0s1
```

Then execute the following command to set the label:
```
bless --folder /Volumes/EFI/EFI/BOOT --label "Kubuntu"
```
or switch out `Kubuntu` with the label of your distribution, if you are using something else.
## Icons
To set an icon for the volume, retrieve your icon of choice in the `.icns` format. Then:
- Put the icon in the top directory of the volume that the bootloader of Linux is on. Rename it `.VolumeIcon.icns`. 
- Alternatively, look at the properties of the EFI volume and drag the icon to the icon area. It will then appear as the icon for that disk's boot option.

## Disk manager as default at boot
Further, we can configure the computer to always boot into the startup disk manager in order to select which OS to boot into at startup. To do so, we want to add a NVRAM parameter. Run the following command as root:
```
nvram manufacturing-enter-picker=true
```

Without this, after installing Linux on a dual-boot setup on a Mac, the Linux partition will automatically be the default startup disk. You can also switch the default startup disk back to macOS, by opening System Settings, navigating to **Startup Disk** and just selecting **Macintosh HD**.

**Sources:**
- [https://wiki.t2linux.org/guides/startup-manager/](https://wiki.t2linux.org/guides/startup-manager/)
- [https://osxdaily.com/2021/02/26/make-intel-mac-boot-startup-manager/](https://osxdaily.com/2021/02/26/make-intel-mac-boot-startup-manager/)