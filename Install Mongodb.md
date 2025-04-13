### Install MongoDB on Windows 11
* Downlad https://www.mongodb.com/try/download/community
* Install using msiexec.exe as follows (hangs at Time remaining: 17 secs):
```
msiexec.exe /l*v mdbinstall.log  /qb /i mongodb-windows-x86_64-8.0.6-signed.msi SHOULD_INSTALL_COMPASS="0"
```
#### Start MongoDB using command line
* Create folder D:/mongodbdata, Run cmd as Administrator and run following command:
```
"C:\Program Files\MongoDB\Server\8.0\bin\mongod.exe" --dbpath="D:\mongodbdata"
```
