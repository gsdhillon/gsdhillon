### Ubuntu 22.04 LTS

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
```
Run netbean by directly providing jdk path as:
```
./netbeans --jdkhome /usr/appl/open-jdk-9
```



