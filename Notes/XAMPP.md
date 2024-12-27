
You should modify the httpd-vhosts.conf file located in xampp\apache\conf\extra. The one in the 'original' folder is typically kept as a backup or reference.
Copy the original one to drive D:\xampp_backup for backup.

Here's a sample of what you might add to your httpd-vhosts.conf file:
# Existing dummy host configurations (you can keep or remove these as needed)
<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host.example.com
    DocumentRoot "c:/Apache24/docs/dummy-host.example.com"
    ServerName dummy-host.example.com
    ServerAlias www.dummy-host.example.com
    ErrorLog "logs/dummy-host.example.com-error.log"
    CustomLog "logs/dummy-host.example.com-access.log" common
</VirtualHost>

<VirtualHost *:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "c:/Apache24/docs/dummy-host2.example.com"
    ServerName dummy-host2.example.com
    ErrorLog "logs/dummy-host2.example.com-error.log"
    CustomLog "logs/dummy-host2.example.com-access.log" common
</VirtualHost>

# Configuration for your current PHP 5.6.8 application
<VirtualHost *:80>
    ServerAdmin webmaster@ClearStep.local
    DocumentRoot "C:/xampp/htdocs/ClearStep"
    ServerName ClearStep.local
    ErrorLog "logs/ClearStep-error.log"
    CustomLog "logs/ClearStep-access.log" common
    <Directory "C:/xampp/htdocs/ClearStep">
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>

# Configuration for your new Laravel 11 application (to be used with new XAMPP installation)
<VirtualHost *:80>
    ServerAdmin webmaster@newapp.local
    DocumentRoot "D:/xampp/htdocs/newapp/public"
    ServerName newapp.local
    ErrorLog "logs/newapp-error.log"
    CustomLog "logs/newapp-access.log" common
    <Directory "D:/xampp/htdocs/newapp/public">
        Options Indexes FollowSymLinks MultiViews
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>