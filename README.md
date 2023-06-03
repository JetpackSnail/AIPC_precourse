# AIPC_precourse
For course "Automating Infrastructure Provisioning and Configuration"

## Nginx setup

1) Remove the default symlnik install in `/etc/nginx/sites-enabled`

2) Create your own symlink of your nginx configuration file to `/etc/nginx/sites-enabled`

3) Test and restart Nginx server

## MySQL setup

1) Stop MySQL and disable autostart
```
sudo systemctl stop mysql.service
sudo nano /etc/init/mysql.conf
```

2) [Mirgration of MySQL folders]([https://www.digitalocean.com/community/tutorials/how-to-move-a-mysql-data-directory-to-a-new-location-on-ubuntu-20-04])
```
sudo mysql
SELECT @@datadir;
```

## Configure firewall

1) Enable firewall
```
sudo ufw enable
```

2) Add rules
```
sudo ufw allow http
sudo ufw allow https
sudo ufw allow OpenSSH
sudo ufw allow 3306
```

3) Check rules
```
sudo ufw status
```
