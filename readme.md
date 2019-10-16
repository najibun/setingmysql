## Seting mysql databse
1. Masuk ke mysql dengan root
```
 mysql -u root -p
 ``` 
 2. Membuat database

**Pastikan** untuk merubah **nama_database** sesuai yang anda inginkan.
```
create database nama_database;
``` 
 4. Grant database (membuat akses)

**Pastikan** untuk merubah **user** dan **password** sesuai dengan kebutuhan.
```
grant all on nama_database.* to user@localhost identified by "password";
grant all on nama_database.* to user@`127.0.0.1` identified by "password";
```
 6. Flush config mysql
```
flush privileges;
```
2. Untuk keluar dari mysql ketik
```
\q
```

**Berikut contoh ketika menjalankan grant ini.**
```
$ mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 326421
Server version: 5.1.73 Source distribution

Copyright (c) 2000, 2013, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> create database omeka;
Query OK, 1 row affected (0.02 sec)

mysql> grant all on omeka.* to omeka@localhost identified by "omekaPASS";
Query OK, 0 rows affected (0.18 sec)

mysql> grant all on omeka.* to omeka@`127.0.0.1` identified by "omekaPASS";
Query OK, 0 rows affected (0.00 sec)

mysql> flush privileges;
Query OK, 0 rows affected (0.18 sec)

mysql> \q
Bye
$
```
