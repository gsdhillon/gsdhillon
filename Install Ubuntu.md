### Ubuntu 22.04 LTS

#### Fix problem - Wireless Mouse not working smoothly
```
sudo nano /etc/default/grub
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash i8042.nomux i8024.noloop"
sudo update-grub
-- restart the PC
```



####  Install Google Chrome
```
sudo apt install wget
```
```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```
```
sudo dpkg -i google-chrome-stable_current_amd64.deb 
```



