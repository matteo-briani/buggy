# Buggy

Hacked version of the Panther Classic from Gig Nikko.

## OS
The Os is the Raspian Lite OS. 
First steps for the headless Pi are:
- add an empty ```ssh``` file in ```/boot```
- add ```wpa_supplicant.conf``` in ```/boot```
- change the hostname to something more meaningful than "rapsberry" (optional)


## Power supply
A step down DC-DC converter from a LiPo 7.4 battery to 5v directly connected to the 5v power rail of the RPi.
 

## Misc

First experimentation with the Arduino motor shield are from [this page](http://blog.janlipovsky.cz/2016/03/robocar-arduino-motor-shield-with-raspberry-pi-part2.html).
Since it uses two power supplies (ICs and motors) remove the PWR jumper.


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

## Hardware specs

Using a single 7.4v LiPo battery (measured 8.4 volts fully charged) the motors give the following results:
- The steering solenoid is drawing 250mA
- The rear motor is drawing 250mA, but goes quickly to 2A if put under load

