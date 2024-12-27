One time process to run MySQL concurrently
Install the Services:

mysqld --install mysqld3306 --defaults-file="C:\xampp\mysql\bin\my.ini"

mysqld --install mysqld3307 --defaults-file="D:\xampp\mysql\bin\my.ini"

net start mysqld3306
net start mysqld3307

SELECT TABLE_NAME, ENGINE
    -> FROM INFORMATION_SCHEMA.TABLES
    -> WHERE TABLE_SCHEMA = 'portfolio_development'
    ->   AND TABLE_NAME = 'dividends';

mysql -u root -p -P 3307 portfolio_development < C:\Backup\mysql\portfolio_development_Oct-31.sql

C:\Windows\System32>d:

D:\>cd xampp\mysql\bin

D:\xampp\mysql\bin>mysql -u root -p -P 3307
Enter password: