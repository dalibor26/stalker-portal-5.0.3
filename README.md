# Stalker Portal 5.0.3 install on Ubuntu 14.04 LTS / 16.04 LTS

Stalker Portal auto install script on Ubuntu 14.04 LTS / 16.04 LTS

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/DaliborVidovic?country.x=BA&locale.x=en_US)  You can make one-time donations via PayPal.

##### Runs on
[![Ubuntu](https://user-images.githubusercontent.com/12951085/139538206-833d8d33-0d1b-4d51-8ec8-86e5cf14f82e.png)](https://www.ubuntu.com)

This script work only on Clean Ubuntu 14.04 LTS / 16.04 LTS

Version PHP5

Stalker auto install script
  * Version of Stalker 5.0.3

## Installation
```bash
apt-get install git
git clone https://github.com/dalibor26/stalker-portal-5.0.3.git
cd stalker-portal-5.0.3/
```

Open stalker_portal_5.0.3.sh with your favorite text editor and change on line 11
```bash
mysql_root_password="firefly26"
```
This is the root password for MySQL that will be set during the installation, you can change it with yours if you wish.


And on line 10 change
```bash
TIME_ZONE="Europe/Berlin"
```
This is the time zone that will be set during the installation, you can change it with yours if you wish

The installation itself is as follows:
```bash
chmod +x stalker_portal_5.0.3.sh
./stalker_portal_5.0.3.sh
```
Accordingly, during the installation, when executing the last command, phing will ask you for the root password for MySQL, enter the password you set on line 11



You can access your stalker portal at: http://ipaddress/stalker_portal The username and password to login to the portal are your default
```
Login: admin
pass: 1
```

Remove all test channels from the database through the terminal
```bash
mysql -u root -p stalker_db
truncate ch_links;
truncate itv;
```


[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/DaliborVidovic?country.x=BA&locale.x=en_US)  You can make one-time donations via PayPal.
