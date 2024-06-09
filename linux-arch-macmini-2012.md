## install linux-arch

run command `archinstall`, config it.

```bash
archinstall
```

## setup wifi

### install b43-firmware

```bash
git clone https://aur.archlinux.org/b43-firmware.git
cd b43-firmware
makepkg -si
```

### load and config b43 module

```bash
sudo modprobe b43
nmtui
```

### remove b43 from blacklist

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

## setup fish

### install fish

```bash
sudo pacman -S fish
chsh -s /usr/bin/fish
```

### install fisher

```bash
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```

### install dracula theme

```bash
fisher install dracula/fish
fish_config theme choose "Dracula Official"
```

### install fonts

```bash
sudo pacman -S terminus-font 
sudo setfont ter-v18b
sudo nano /etc/vconsole.conf
```

edit

```bash
FONT=ter-v18b
```
