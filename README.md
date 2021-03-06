# linux_server_config
## Udacity Linux Server Configuration Project
## 1. IP: 13.228.229.122:2200
## 2. URL: http://13.228.229.122/
## 3. Installed:
  1. PostgreSQL 9.5
  2. Python 2.7.12
    a. Flask
    b. Flask-SeaSurf
    c. SQL Alchemy
    d. OAuth2Client
## 4. Update all currently installed packages
1. sudo apt-get update
2. sudo apt-get upgrade

## 5. Change the SSH port from 22 to 2200
1. 'sudo nano /etc/ssh/sshd_config' and then change the port listener from 22 to 2200
2. Reload SSH with 'sudo service ssh restart'

## 7. Configure the Uncomplicated Firewall
1. Install ufw with 'apt-get install ufw'
2. Set up default policies to deny incoming and allow outgoing
  a. sudo ufw default deny incoming
  b. sudo ufw default allow outgoing
3. Set up allowed connections
  a. 'sudo ufw allow 2200' --SSH
  b. 'sudo ufw allow 80' --HTTP
  c. 'sudo ufw allow 123' --NTP
4. Start UFW up with 'sudo ufw enable'

## 8. References
1. http://bodhizazen.com/Tutorials/SSH_keys#Generate
2. http://linuxproblem.org/art_9.html
3. https://help.ubuntu.com/lts/serverguide/NTP.html
4. https://devops.profitbricks.com/tutorials/install-and-configure-mod_wsgi-on-ubuntu-1604-1/
5. https://stackoverflow.com/questions/9353822/connecting-postgresql-with-sqlalchemy
