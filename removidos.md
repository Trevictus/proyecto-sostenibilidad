* vlc
* cups
* build-essentials


Seguir usando PowerTop
powertop
sudo systemctl stop apt-daily.timer
sudo systemctl disable apt-daily.timer

BLUETOOTH
sudo systemctl stop bluetooth
sudo systemctl disable bluetooth

UI
sudo apt-get remove --purge lxde

HDMI
/usr/bin/tvservice -o
