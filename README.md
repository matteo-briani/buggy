# Buggy

Hacked version of the Panther Classic from Gig Nikko.

## OS
The Os is the Raspian Lite OS. 
First steps for the headless Pi are:
- add an empty ```ssh``` file in ```/boot```
- add ```wpa_supplicant.conf``` in ```/boot```
- change the hostname to something more meaningful than "rapsberry" (optional)



## Misc

First experimentation with the Arduino motor shield are from [this page](http://blog.janlipovsky.cz/2016/03/robocar-arduino-motor-shield-with-raspberry-pi-part2.html).


```wpa_supplicant.conf``` template

```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
ap_scan=1
fast_reauth=1
country=JP

network={
	ssid="Your SSID"
	psk="Your password"
	id_str="0"
	priority=100
}
```


