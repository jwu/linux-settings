### install & config gnome extensions

```bash
sudo apt update 
sudo apt install gnome-tweaks 
sudo apt install gnome-shell-extensions 

gsettings set org.gnome.desktop.peripherals.keyboard delay 300
gsettings set org.gnome.desktop.peripherals.keyboard repeat-interval 30
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

### install onedrive

```bash
# install dependency
sudo apt install build-essential
sudo apt install libcurl4-openssl-dev libsqlite3-dev pkg-config git curl
curl -fsS https://dlang.org/install.sh | bash -s dmd
sudo apt install libnotify-dev

# compile onedrive
git clone https://github.com/abraunegg/onedrive.git
cd onedrive

# Run `source ~/dlang/dmd-2.108.1/activate.fish` in your shell to use dmd-2.108.1.
# This will setup PATH, LIBRARY_PATH, LD_LIBRARY_PATH, DMD, DC, and PS1.
source ~/dlang/dmd-2.108.1/activate.fish

./configure
make clean; make;
sudo make install

# Run `deactivate` later on to restore your environment.
deactivate

# first time sync
cp ./config/onedrive ~/.config/onedrive/config
onedrive --synchronize

# create service
cp ./service/onedrive.service /etc/systemd/system/onedrive.service
sudo systemctl daemon-reload
sudo systemctl enable onedrive
sudo systemctl start onedrive
```

### update desktop apps

```bash
cp ./desktop/godot.desktop ~/.local/share/applications/godot.desktop
cp ./desktop/blender.desktop ~/.local/share/applications/blender.desktop
update-desktop-database ~/.local/share/applications/
```

### desktop apps

- [Obsidian](https://obsidian.md/download)
- [draw.io](https://www.drawio.com/)
- [Godot](https://godotengine.org/download/linux/)
- [Blender](https://www.blender.org/download/)
- [Krita](https://krita.org/)
- [Telegram Desktop](https://desktop.telegram.org/)
- [Discord Desktop](https://discord.com/download)
- [VLC](https://www.videolan.org/)
- [MDC](https://github.com/mvdctop/Movie_Data_Capture/releases)
