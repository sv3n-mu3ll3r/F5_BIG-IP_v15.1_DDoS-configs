BIG-IP_DDoS-config
this repository contains F5 BIG-IP DDoS startup configs


=========================================================================

sVen_Device-DoS_15_1.conf: 
This file contains a startup Device-DoS config for BIG-IP L3/4 DDoS (AFM/DHD). It was created on TMOS version 15.1

You can simply merge the config snippet by using the 'tmsh merge' command.
Example: 

$ tmsh load sys config verify merge file /config/sVen_Device-DoS_15_1.conf
and when succesfull: 
$ tmsh load sys config merge file /config/sVen_device-DoS_15_1.conf

For the bad_ACK vector you need to add your vlans.

=========================================================================


