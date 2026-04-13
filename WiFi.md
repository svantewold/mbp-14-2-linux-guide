## 1. Check the network controller
In a terminal, run:
```
lspci -nn -d 14e4:
```

The output will look similar to the following:
```
02:00.0 Network controller [0280]: Broadcom Inc. and subsidiaries BCM43602 802.11ac Wireless LAN SoC [14e4:43ba] (rev 02)
```
## 2. Installing the proper WiFi driver
Check [this link](https://askubuntu.com/questions/55868/installing-broadcom-wireless-drivers) to find the proper WiFi driver for your specific network controller.

Then, run the following commands as root:
```
apt update
update-pciids
apt install <PACKAGE_NAME>
```

where you replace `<PACKAGE_NAME>` with the proper driver package name you found via the link above. For a MacBook Pro 14,2 the proper driver package is `firmware-b43-installer`. Then, reboot by running `reboot` as root.
## 3. Resolving connectivity issues
Download `brcmfmac43602-pcie.txt` [here](https://bugzilla.kernel.org/attachment.cgi?id=285753)

Open it, and change the lines:
```
macaddr=xx:xx:xx:xx:xx:xx
ccode=X3
regrev=15
```

to the following:
```
macaddr=00:90:4c:0d:f4:3e
ccode=0
regrev=1
```

Then, copy the file to the correct place in a terminal by running (as root):
```
cp ~/Downloads/brcmfmac43602-pcie.txt /lib/firmware/brcm/
```
then make sure to reboot again. After booting up again, the WiFi connection should work. Remember to activate the [firewall](Firewall.md)!

**Source:**
- https://askubuntu.com/questions/55868/installing-broadcom-wireless-drivers