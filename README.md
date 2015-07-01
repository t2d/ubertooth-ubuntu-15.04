# ubertooth-ubuntu-15.04
Writeup about what is different in Ubuntu 15.04 from the general [build instructions](https://github.com/greatscottgadgets/ubertooth/wiki/Build-Guide).

## Kismet
Ubuntu 15.04 alread brings the correct version of kismet.
Install with
```
sudo apt install kismet
```

Add the plugins with
```
cp kismet-plugins/ubertooth.so ~/.kismet/plugins/
cp kismet-plugins/ubertooth_ui.so ~/.kismet/client_plugins/
```

## Udev
Ubuntu uses 'plugdev' as group for usb permissions. Copy them with
```sudo cp 40-ubertooth.rules /etc/udev/rules.d/
```
Log out and in to get correct permissions.
Also deattach and reattach the ubertooth. 
