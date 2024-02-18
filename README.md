Stalker Portal 5.0.3 install on Ubuntu 20.04 LTS / 18.04 LTS

Stalker Portal auto install script on Ubuntu 20.04 LTS / 18.04 LTS

Donate You can make one-time donations via PayPal.
Runs on

Ubuntu

This script work only on Clean Ubuntu 20.04 LTS / 18.04 LTS

Stalker auto install script

    Version of Stalker 5.0.3

Installation

apt-get install git
git clone https://github.com/@dalibor26/stalker-portal-5.0.3.git
cd stalker-portal-5.0.3/

Open stalker_portal_5.0.3.sh with your favorite text editor and change on line 11

mysql_root_password="test123456"

This is the root password for MySQL that will be set during the installation, you can change it with yours if you wish.

And on line 10 change

TIME_ZONE="Europe/Berlin"

This is the time zone that will be set during the installation, you can change it with yours if you wish

The installation itself is as follows:

chmod +x stalker_portal_5.0.3.sh
./stalker_portal_5.0.3.sh

Accordingly, during the installation, when executing the last command, phing will ask you for the root password for MySQL, enter the password you set on line 11

You can access your stalker portal at: http://ipadres/stalker_portal The username and password to login to the portal are your default

Login: admin
pass: 1

Remove all test channels from the database through the terminal

mysql -u root -p stalker_db
truncate ch_links;
truncate itv;
