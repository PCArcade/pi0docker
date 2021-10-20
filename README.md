# pi0docker
## pi-hole for PiZero

### If you have an adafruit minipitft and want pi-hole to display stats to the following  :
  
Install Python3  
edit /etc/rc.local and add:  
```
docker-compose -f ~pcarcade/pi0docker/docker-compose.yml up -d
sudo python3 path/to/stats.py &
```
The docker-compose line makes sure that pi-hole and stats.py run in the same session  
Probably shouldn't be needed but it doesn't seem to work without it
  
When the pi0 is booted the IP address will be displayed on the screen, set either your routers DNS to this, ot the DNS field on the device you want to block ads on
  
Admin and DHCP etc can be administered at http://pi-hole.local/admin 
