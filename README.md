### install & config gnome extensions

```bash
sudo apt update 
sudo apt install gnome-tweaks 
sudo apt install gnome-shell-extensions 

gsettings set org.gnome.desktop.peripherals.keyboard delay 300
gsettings set org.gnome.desktop.peripherals.keyboard repeat-interval 20
```

### install pyenv

```bash
curl https://pyenv.run | bash
```

### install nvm

```bash
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
fisher install jorgebucaran/nvm.fish
nvm install latest
```

### install nvim

```bash
sudo cp -r nvim-linux64/bin/ /usr/
sudo cp -r nvim-linux64/lib/ /usr/
sudo cp -r nvim-linux64/share/ /usr/
```

### install neovide

```bash
sudo cp neovide-linux-x86_64/neovide /usr/bin/
sudo desktop-file-install neovide.desktop
sudo update-desktop-database
```

### install utils

```bash
cargo install btm
cargo install procs
cargo install du-dust
curl -sfL https://raw.githubusercontent.com/ducaale/xh/master/install.sh | sh
sudo apt install fd-find
```

### update desktop apps

```bash
cp godot.desktop ~/.local/share/applications/godot.desktop
cp blender.desktop ~/.local/share/applications/blender.desktop
update-desktop-database ~/.local/share/applications/
```
