# UpdateTransmissionPort
OpenVPN/Private Internet Access(PIA)/Transmission Port Update script

Pieced together with a few scripts found around the 'net and modified to work with FreeNas instance of transmission

If you need an excellent guide use this one: https://forums.freenas.org/index.php?threads/guide-setting-up-transmission-with-openvpn-and-pia.24566/ 

## Install
Copy this script into a location on the transmission jail. If you took my advice and used the above guide it is advisable to place the script here: /usr/local/etc/openvpn/updateTransmissionPort.sh

## Create Cron
Once you have the script in the jail you will need to add a cron job. 

Just follow these steps;
```
nano /etc/crontab
```

add a new cron
```
# Update Transmission port
15  * * * * root /usr/local/etc/openvpn/updateTransmissionPort.sh
```
This will run 15 minutes after each hour
