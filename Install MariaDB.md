### Install MariaDB 10 on Windows
* Download MariaDB Server 10.4.7 msi setup and install.
* Add MariaDB Server 10.4.7 in system path env.
* on cammand prompt run follwing command to check:
```
mysql -u root -p
```
* Heidi SQL will be installed auomatically along with MariaDB.

### Install MariaDB 10 on Ubuntu
```
sudo apt update
sudo apt install mariadb-server
sudo mysql_secure_installation
```
* Important entries:
1. Switch to unix_socket authentication [Y/n] n
2. Change the root password? [Y/n] y
3. Remove anonymous users? [Y/n] y
4. Disallow root login remotely? [Y/n] n
5. Remove test database and access to it? [Y/n] y
6. Reload privilege tables now? [Y/n] y

#### Restore database backup
1. Open MySQL shell and create datbase
```
mysql -u root -p
> create database myonlineexam;
> exit
```
2. Restore database backup
```
mysql -u root -p myonlineexam < ~/MyOnlineExam/myonlineexam.sql
```
3. Resolving unknown collation error comes with follwing message:
```
ERROR 1273 (HY000) at line 273: Unknown collation: 'utf8mb4_0900_ai_ci'
```
4. Check how many times this collation is used
```
cat ~/MyOnlineExam/myonlineexam.sql | grep utf8mb4_0900_ai_ci
```
5. Replace utf8mb4_0900_ai_ci with utf8mb4_general_ci using sed stream editor.
```
sed -i 's/utf8mb4_0900_ai_ci/utf8mb4_general_ci/g' ~/MyOnlineExam/myonlineexam.sql
```
6. Try the restore back command again.

#### Taking backup 
``` 
mysqldump -u root -p myonlineexam > ~/MyOnlineExam/myonlineexam.sql
```
* Push the myonlineexam.sql file immediately to the server (github etc.)

#### Resolve Table Names Case Senstivity Problem - On Linux

```
sudo nano /etc/mysql/conf.d/mysql.cnf
```
- Under [mysql] section make another section [mysqld] and enter line: lower_case_table_names=1
- Content of mysql.cnf may look like :
```
[mysql]

[mysqld]
lower_case_table_names=1
```
Restart the mariadb service and check the value of lower_case_table_names as follow:
```
systemctl restart mariadb
sudo mysqladmin -u root -p variables | grep lower_case_table_names
```

---
#### Connect MySQL with Netbeans
1. Open Services > Databases > Drivers > MySQL (Connector/J Driver)
2. Click Add button and provide path to jar file: /home/gurmeet/MyOnlineExam/jars/mysql-connector-java-8.0.17.jar
3. Click Next. Enter database Host: localhost, Port: 3306, Database: myonlineexam, User: root, Pass: Fw0rkal$ and click Test Connection.
4. Click Finish












