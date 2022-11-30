## General packages
sudo dnf install -y vim zsh git fcitx5 fcitx5-mozc fcitx5-autostart fcitx5-configtool gnome-tweaks ulauncher

## Input method
sudo dnf remove ibus-anthy

sudo alternatives --config xinputrc

## xremap
$ sudo dnf install rust cargo
sudo cargo install xremap --features gnome


## Install Chrome

## Install code
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'

sudo dnf check-update
sudo dnf install code
```

 ## Install AWS CLI
[AWS CLI の最新バージョンをインストールまたは更新します。 - AWS Command Line Interface](https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions)

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

## Install Session Manager Plugin

[Official Docs](https://docs.aws.amazon.com/ja_jp/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html#install-plugin-linux)

```bash
curl "[https://s3.amazonaws.com/session-manager-downloads/plugin/latest/linux_64bit/session-manager-plugin.rpm](https://s3.amazonaws.com/session-manager-downloads/plugin/latest/linux_64bit/session-manager-plugin.rpm)" -o "session-manager-plugin.rpm"
sudo dnf install -y session-manager-plugin.rpm
```

## Install docker
[Docker Engine インストール（Fedora 向け） | Docker ドキュメント](https://matsuand.github.io/docs.docker.jp.onthefly/engine/install/fedora/)

```
sudo dnf -y install dnf-plugins-core
sudo dnf config-manager \
    --add-repo \
    https://download.docker.com/linux/fedora/docker-ce.repo

sudo dnf install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```
sudo dnf -y install docker-compose
```

```
sudo systemctl start docker
sudo systemctl enable docker
```

