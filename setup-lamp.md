## Step 1: Add new local domain
sudo gedit /etc/hosts

Step 1: cd /etc/apache2/sites-available/
Step 2: sudo cp 000-default.conf majestic.localhost.conf
Step 3: sudo gedit majestic.localhost.conf
Step 4: Paste ....[code]
Step 5: sudo a2ensite majestic.localhost.conf
Step 6: sudo service apache2 restart 


[code]
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    DocumentRoot /home/truongnn/projects/eva-corp/public_html
    ServerName evacorp.localhost
    ErrorLog ${APACHE_LOG_DIR}/evacorp-error.log
    CustomLog ${APACHE_LOG_DIR}/evacorp-access.log combined
    <Directory //home/truongnn/projects/eva-corp/public_html/>
        Options Indexes FollowSymLinks
        AllowOverride All 
        Require all granted
        allow from all
    </Directory>
</VirtualHost>
