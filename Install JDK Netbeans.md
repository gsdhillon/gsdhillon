### Install on Windows 11
* From Administrator A/C : Settings > Apps > Apps Adv Settings > Where to get apps [Anywhere] 
* Download jdk21.exe and install
* Download Netbeas25.exe and install. Open notepad as Administrator > open C:Prog..Files/Netbeans/etc/netbeans.conf and following :
```
netbeans_default_options="-J-Xms256m -J-Xmx2048m -J-XX:MaxPermSize=256m ...... keep other params "
```
* Install Tomee separately and use Add Server.
  

# Ubuntu

####  Install Open JDK-9
- Download https://download.java.net/java/GA/jdk9/9.0.1/binaries/openjdk-9.0.1_linux-x64_bin.tar.gz    - size 206 MB
```
cd /usr
sudo mkdir appl
cd appl
sudo tar -xvf ~/Downloads/openjdk-9.0.1_linux-x64_bin.tar.gz
sudo mv jdk-9.0.1 open-jdk-9
```

####  Install Apache Netbeans-15
- Download https://dlcdn.apache.org/netbeans/netbeans/15/netbeans-15-bin.zip    -  size 435MB
```
cd /usr/appl
sudo unzip ~/Downloads/netbeans-15-bin.zip 
./netbeans --jdkhome /usr/appl/open-jdk-9
```
##### Create Desktop Shortcut for Netbeans
1. Create a file named Netbeans.desktop at ~/Desktop
```
cd ~/Desktop
gedit Netbeans.desktop
```
2. Enter following text in Netbeans.desktop
```
#!/usr/bin/env xdg-open
[Desktop Entry]
Version=1.0
Type=Application
Terminal=false
Exec=/usr/appl/netbeans/bin/netbeans --jdkhome /usr/appl/open-jdk-9
Name=Nebeans
Comment=Apache Netbeans 15
Icon=/usr/appl/netbeans/nb/netbeans.icns
```
3. Right click on the icon and Allow Launching'

