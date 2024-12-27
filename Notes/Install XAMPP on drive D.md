Follow these simple instructions to install XAMPP Server on Windows 11: 
1. **Download XAMPP Installer**: Start by downloading the XAMPP installer from the official Apache Friends website. Visit [https://www.apachefriends.org/index.html](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbTZLNnZ4UTJVMUROejlzcm5xWGR4MzU2bWN5UXxBQ3Jtc0ttTXJ4SlpsZ05PUE82MkViTThyOFRhb2xyUmlnU1VFcUZ1bzJEUWJPUzJoOE85bEVvOU1DLTI3Qzc0cGhjdXJZVGxtcVJzeFduTjJ4NjlBQlk5TFlpV3FBQmI5WWs0alFTUS1uOEhZOFozQmVKbnhVTQ&q=https%3A%2F%2Fwww.apachefriends.org%2Findex.html&v=G2VEf-8nepc) and click on the "Download" button for the latest version of XAMPP. 
2. **Run the Installer**: Once the download is complete, locate the downloaded XAMPP installer file (e.g., "xampp-windows-x64-x.x.x-installer.exe") and double-click on it to run the installer. 
3. **User Account Control (UAC) Prompt**: If prompted by User Account Control (UAC), click "Yes" to allow the installer to make changes to your device. 
4. **Select Components**: In the XAMPP Setup wizard, select the components you want to install. By default, Apache, MySQL, PHP, and phpMyAdmin are selected. You can also choose additional components based on your requirements. 
5. **Choose Installation Directory**: Choose the directory where you want to install XAMPP. The default directory is "D:\xampp", but you can select a different location if needed. 
6. **Start the Installation**: Click on the "Next" button to start the installation process. The installer will extract and install the selected components to the specified directory. 
7. **Complete the Installation**: Once the installation is complete, you'll be prompted to launch the XAMPP Control Panel.  580MB & 8,000 files
8. Open xampp-control.exe. 9
9.  Click config of MySql and edit my.ini by changes all 3306 to 3307 & 
	add this statement to innodb statements group
		innodb_force_recovery=1 

10. Click config of Apache and edit httpd.conf by changes all port 80 to port 8080 e.g. Listen 80, ServerName localhost:8080, ServerName www.example.com:8443

11.  Click config of Apache and edit httpd-ssl.conf by changes all port 443 to port 8443 e.g. Listen 8443, <VirtualHost _default_:8443>
12. Check and modify the D:\xampp\phpMyAdmin\config.inc.php: 
	\$cfg['Servers'][$i]['host'] = '127.0.0.1';
	\$cfg['Servers'][$i]['port'] = '3307';  // Make sure this matches new MySQL port
	
13. **Start Apache and MySQL**: In the XAMPP Control Panel, start the Apache and MySQL services by clicking on the "Start" buttons next to their respective names. You may also want to configure XAMPP to start automatically with Windows by checking the "Svc" boxes.  
14.  **Verify Installation**: Open your web browser and navigate to http://localhost:8080/. If XAMPP is installed correctly, you should see the XAMPP dashboard, indicating that Apache and MySQL are running.