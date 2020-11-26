# lightning atm

## item list

Based on this [list](https://docs.lightningatm.me/requirements/hardware-requirements), however without the camera and button.

* raspberry
  * wifi adapter if raspberry is older and has none
* display
  * band cable \(between display and display platine\)
  * jumper cables to connect to raspberry
* case
* coin acceptor
  * jumper cables to connect to raspberry
* power supply \(rasperry needs 5V, coin acceptor needs 12V\)
  * 5 -&gt; 12 V transformer
  * micro usb .... wip

#### tools

* screw driver
* Blu-Tack
* Swiss army knife
* coins for coin acceptor

## raspberry

* [Doc Tutorial](https://docs.lightningatm.me/lightningatm-setup/hardware-setup/assembly-and-software)

### setup

* [Video at setup position ](https://youtu.be/A9JKUQvvmYM?t=557)

### **connect**

1. IP addresse herausefinden: `$ raspberrypi.local` Sollte den Raspberry finden und anpingen.
2. Mit SSH verbinden: `$ ssh pi@ip_address`  Passwort: l1ghtning

* `$ sudo poweroff` \(erst vom Netz nehmen, wenn grünes Lämpchen nicht mehr leuchtet\)
* `$ sudo reboot`

### pins

![Raspberry Pins](https://www.elektronik-kompendium.de/sites/raspberry-pi/fotos/raspberry-pi-15b.jpg)

### tmux

To be able to have multiple consoles open with ssh, the program `tmux` is used. Primarily to monitor the log file while simultaneously be able to enter commands.

[Doc Tutorial](https://docs.lightningatm.me/lightningatm-setup/software-setup/monitoring_log_file)

## display

[Doc Tutorial](https://docs.lightningatm.me/lightningatm-setup/hardware-setup/raspberry-pi-and-display)

## coin acceptor

[ Doc Tutorial](https://www.youtube.com/watch?v=14JfEhNSdZE&feature=youtu.be)

## power supply

_wip_

_Tricky part is to be able to supply both raspberry and coin acceptor with one cable._

## wallet

_wip_

## references

{% embed url="https://docs.lightningatm.me/" %}

{% embed url="https://github.com/21isenough/LightningATM" %}

{% embed url="https://blog.fulmo.org/the-lightningatm-pocket-edition/" caption="Pocket Edition" %}



