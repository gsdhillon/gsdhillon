### Ubuntu 22.04 LTS

####  Install Google Chrome
```
sudo apt install wget
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb 
```

#### Install Pinta for Image Editing
-- Useful to crop imaging, making transparent images, adding some text on images etc.
-- Selecting boundary is nice
```
sudo apt install pinta
```

#### Install Word Dictionary
```
sudo apt install goldendict
```
- Will take 1-2 minutes to install
- Hotkeys ctrl+C+C  Press and hold ctrl and type C twice with any delay in between

#### Commands
* CTRL + L to see/copy path of file explorer
```
free -m
vmstat -s
top –i    ---- cntl + C to exit
systemctl start/stop/restart/enable/disable servicename
ls -la ~/MyOnlineExam/ | grep .sql
```

#### Fix problem - Wireless Mouse not working smoothly
- First try to change usb port. Preferably at front side.
- Check battery of the mouse also. Mouse consumes more battery than keyboard.
- If stillslow try to change following settings.
```
sudo nano /etc/default/grub
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash i8042.nomux i8024.noloop"
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash irqpoll"
sudo update-grub
-- restart the PC
```

#### Install lm-sensors to monitor PC hardware
```
sudo apt-get install lm-sensors
sudo sensors-detect
sudo nano /etc/sensors3.conf
sensors
```
- Use sesonrs command to monitor CPU temp. etc.

#### Fix problem - SNMP Restart
```
sudo nano /etc/rc.local
service snmpd restart
```



