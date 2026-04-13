## 1. Installing Flatpak and the backend for Plasma Discover
We want to install the Flatpak package as well as the package for the Flatpak backend for Plasma Discover. This can be done directly in Plasma Discover, or in the terminal (as root):
```
apt install flatpak plasma-discover-backend-flatpak
```
## 2. Integrating Flatpak support into Plasma System Settings
In a terminal, run (as root):
```
apt install kde-config-flatpak
```
## 3. Add the Flathub repository
This can be done in the settings in Plasma Discover, or in a terminal by running:
```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

**Source:**
- [https://flatpak.org/setup/](https://flatpak.org/setup/)