### Install MongoDB on Windows 11
* Downlad https://www.mongodb.com/try/download/community
* Install using msiexec.exe as follows (hangs at Time remaining: 17 secs):
```
msiexec.exe /l*v mdbinstall.log  /qb /i mongodb-windows-x86_64-8.0.6-signed.msi ADDLOCAL="ServerService" SHOULD_INSTALL_COMPASS="0"
```
* Add C:\Program Files\MongoDB\Server\8.0\bin in path env.
* Create folder D:/mongodbdata
#### Start MongoDB service
* Run cmd as Administrator and run following command:
```
-- start service. it will use db path as specified in C:\Program Files\MongoDB\Server\8.0\bin\mongod.cfg
net start MongoDB
-- or start from command line itself by specifying path to db
mongod --dbpath="D:\mongodbdata"
```


#### Connect to MongoDB using mongosh
* Doanload mongosh-2.5.0-x64.msi from https://www.mongodb.com/try/download/shell. Run the setup.
* Add C:\Program Files\mongosh in path env.
* Run mongosh on cmd. It showld display following.
```
Current Mongosh Log ID: 67fbe171b82254288bb5f898
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+2.5.0
Using MongoDB:          8.0.6
Using Mongosh:          2.5.0
```
* If Service is not running, it will show following msg:
```
MongoNetworkError: connect ECONNREFUSED 127.0.0.1:27017
```
