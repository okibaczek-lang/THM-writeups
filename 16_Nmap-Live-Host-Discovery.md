# THM - Nmap Live Host Discovery

## Subnet & ARP
Subnet = own network segment connected via router
ARP scan works only within your subnet
nmap -PR -sn TARGET     # ARP only scan

## Target Formats
10.11.12.15-20          # range of 6 IPs
IP/30                   # 4 IPs (CIDR)
nmap -iL hosts.txt      # targets from file
nmap -sL TARGETS        # list targets without scanning
nmap -sn TARGETS        # discover hosts, no port scan

## Host Discovery Options
-PE    # ICMP echo request
-PP    # ICMP timestamp request
-PM    # ICMP mask query
-PS    # TCP SYN ping
-PA    # TCP ACK ping
-PU    # UDP ping (no response = host up)

## DNS
-n     # skip reverse DNS lookup
-R     # force reverse DNS lookup

## Key lesson
Test multiple discovery methods —
one might show host as down while another finds 10 hosts.
