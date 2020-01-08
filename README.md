BIG-IP_DDoS-config
this repository contains F5 BIG-IP DDoS startup configs. 
I use this configs as a start for new depleyments.

=========================================================================

sVen_Device-DoS_15_1.conf: 
This file contains a startup Device-DoS config for BIG-IP L3/4 DDoS (AFM/DHD).

For the bad_ACK vector you need to add your vlans.
It was created on TMOS version 15.1

=========================================================================

sVen_DoS_profiles.conf:
This file contains startup DoS profiles for BIG-IP (AFM/DHD). 
It was created on TMOS version 15.1

It contains 5 DoS profiles:

1) DNS_Host_DoS_profile - This profile is to protect a DNS servcer

2) Network_DNS_Net_DoS_profile - This profile is to protect DNS services (wildcard VS/PO)

3) HTTPs_Host_DoS_profile - This profile is to protect a HTTP(s) host.

4) Network_Host_DoS_profile - This profile is to protect a host on the network layer

5) Network_Net_DoS_profile - This is profile is to protect a network (wildcard VS/PO) on the network layer

=========================================================================

additional_DoS_configs.conf:
This file adds additional DoS config changes.

=========================================================================

fastL4_profiles.conf
This file contains fastL4 profiles for TMOS version 15.1:

1) sVen_fastl4_SF_L2 - For stateful traffic in a L2 deployment

2) sVen_fastl4_SF_L3 - For stateful traffic in a L3 deployment

3) sVen_fastl4_SL_L2 - For stateless traffic on a L2 deployment

4) sVen_fastl4_SL_L3 - For stateless traffic on a L3 deployment

=========================================================================

You can simply merge the config snippet by using the 'tmsh merge' command.

Example: 

$ tmsh load sys config verify merge file /config/sVen_Device-DoS_15_1.conf
and when succesfull: 
$ tmsh load sys config merge file /config/sVen_device-DoS_15_1.conf




