# THM - Passive Reconnaissance

## Passive vs Active Recon
Passive = gathering info without sending any traffic
- reading social media, blogs, public records

Active = sending packets to the target
- ping, port scan, DNS queries

## Key Tools

### Whois
whois tryhackme.com

= domain owner, registrar, nameservers

### DNS Lookup
nslookup DOMAIN               - basic DNS query

nslookup -type=TYPE DOMAIN      - specific record type

dig DOMAIN TYPE               - detailed DNS info

### Online Tools
- dnsdumpster.com = subdomains list
- crt.sh = certificate transparency logs = more subdomains
- shodan.io = internet-connected devices and open ports

## Why subdomains matter
Subdomains often have less security than main domain.

Forgotten dev/staging subdomains = easy targets.
