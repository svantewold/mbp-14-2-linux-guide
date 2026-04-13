> [!INFO]
> The audio driver with instructions to install it is from: 
> https://github.com/davidjo/snd_hda_macbookpro
> 
> Note that all terminal commands except `git` and `cd` need to be run as root (`sudo`)!
## 1. Installing dependency packages
Make sure that you have these packages installed:
- `linux-headers-generic`
- `make`
- `patch`
- `wget`

If not, install them by running the following in a terminal:
```
apt install gcc linux-headers-generic make patch wget
```

We will also need the Ubuntu Linux kernel source package. Install it by running:
```
apt install linux-source-6.17.0
```
## 2. Building the driver
First, we need to clone the driver repository from GitHub:
```
git clone
https://github.com/davidjo/snd_hda_macbookpro
```

Then to build, move to the downloaded repository and run the install script:
```
cd snd_hda_macbookpro/
./install.cirrus.driver.sh
```

To finish, reboot. Once the computer is started up again, the internal audio should be working!

**Source:**
- https://github.com/davidjo/snd_hda_macbookpro