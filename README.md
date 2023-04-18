# Automatic-Updates-cron
## How to Configure Automatic Updates using Cronjob
### Installing Cron on Your System
```
sudo apt update && sudo apt upgrade
```
```
sudo apt install cron
```
```	
sudo systemctl enable cron
```
### Where’s the Crontab Configuration File?
```
sudo vim /etc/crontab
```
### Understanding the Crontab file format
```
[minute] [hour] [day_of_month] [month] [day_of_week] [user] [command_to_run]
```
```
sudo vim /etc/crontab
```
```
50 19 * * 3 root /usr/bin/apt update -q -y >> /var/log/apt/automaticupdates.log
0 20 * * 3 root /usr/bin/apt upgrade -q -y >> /var/log/apt/automaticupdates.log
```
