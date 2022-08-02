# ubuntu-change-gdm-background

this script will change the greeting screen where you login to Ubuntu
it works for either 20.04 or 20.10


sudo ./ubuntu-change-gdm-background.sh  /path/to/image.jpeg #  jpeg or png




# do below for Ubuntu 22.04

download tar archive and decompress to file

```
wget -qO -  https://github.com/scottstensland/ubuntu-change-gdm-background/blob/master/ubuntu-gdm-set-background.sh.tar.gz?raw=true |   tar zx --strip-components=1  ./ubuntu-gdm-set-background.sh
```

execute file as root to copy your local file  `/some/cool/image.jpeg` to Ubuntu 22.04 login splash background screen image

```
sudo ./ubuntu-gdm-set-background.sh   --image  /some/cool/image.jpeg
```

Changes will be effective after a Reboot (CTRL+ALT+F1 may show the changes immediately)
If something went wrong, log on to tty and run the below command

```
sudo update-alternatives --quiet --set gdm-theme.gresource /usr/share/gnome-shell/theme/Yaru/gnome-shell-theme.gresource
```
