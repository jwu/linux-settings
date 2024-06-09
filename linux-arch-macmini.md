## install linux-arch

run command `archinstall`, config it.

```bash
archinstall
```

## install b43-firmware

```bash
git clone https://aur.archlinux.org/b43-firmware.git
cd b43-firmware
makepkg -si
```

## load and config b43 module

```bash
sudo modprobe b43
nmtui
```

## remove b43 from blacklist

```bash
sudo nvim /usr/lib/modprobe.d/broadcom-wl.conf
```

remove 

```text
blacklish b43
```

## add it to modules-load

```bash
sudo nano /etc/modules-load.d/b43.conf
```

edit

```text
b43
```
