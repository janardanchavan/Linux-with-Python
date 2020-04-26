# RHEL 5. Network
```
Session 19: Linux Networking Core

check routing information
# route -n

Destination : 0.0.0.0 is called as default gateway which is required to access the outsider world.

Delete routing informaton
# route del -net 0.0.0.0
Note you will not be able to access the internet or ping the google.

Add routing back
# route add -net 0.0.0.0 gw 10.0.2.2
Note last ip will be of your hotspot or mode.
```
