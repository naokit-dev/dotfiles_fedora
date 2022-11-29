## 
sudo dnf install -y vim zsh git fcitx5 fcitx5-mozc fcitx5-autostart fcitx5-configtool gnome-tweaks ulauncher

## Input method
sudo dnf remove ibus-anthy

sudo alternatives --config xinputrc

## xremap
$ sudo dnf install rust cargo
sudo cargo install xremap --features gnome


## Install Chrome

## INstall code
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update
sudo dnf install code
```
