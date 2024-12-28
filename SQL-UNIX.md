#MYSQL INSTALATION AND CONFIGURATION

```bash
sudo apt install mysql-server
sudo service mysql status
sudo ss -tap | grep mysql
sudo service mysql restart
sudo journalctl -u mysql
sudo systemctl restart mysql.service
```

# MySQL Command Line Client
```SQL
show databases;
use DB_Name;
show tables;

SELECT * FROM Table_Name;
``` 
