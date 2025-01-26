# Alfa-AWUS036AXM-Kali-Linux-
This post is the guide to make the ALFA AWUS036AXM wifi and bluetooth adapter to work 

Basically the Alfa AWUS036AXM is a WiFi adapter with Built-in Bluetooth chip

To make this Run in Kali Linux, we need to make sure that the bluetooth is disabled and is not used by the network adapter, for this,

### run the following commands: 

`sudo systemctl status bluetooth`

it should show disabled, if not then ,

`sudo systemctl stop bluetooth`
`sudo systemctl disable bluetooth`

This should diable the bluetooth

Permanent Disable: To prevent Bluetooth from loading after a reboot, you can blacklist the Bluetooth driver:

Edit the blacklist file:

`sudo nano /etc/modprobe.d/blacklist.conf`

Add the following line at the end:

`blacklist btusb`

Reboot: 

`sudo reboot now` or `sudo reboot`

Check:

`lsusb` or `sudo airmon-ng` or `iwconfig`

These commands will show the mediatek drivers which means you are now ready to use Alfa AWUS036AXM Network Adapter.

if you are facing any issues, open the query in github 

Thank you!
