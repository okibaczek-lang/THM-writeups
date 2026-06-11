# THM - Active Reconnaissance

## What is Active Recon
Sending packets to the target to gather information.
Harder to hide than passive recon.

## Browser Tools
- FoxyProxy = switch between Burp/ZAP proxy quickly
- User Agent Switcher = emulate different browsers
- Wappalyzer = detect technologies used on site

## Key Commands

### Ping
ping TARGET                - check if host is up

ping -c 5 TARGET           - send 5 packets only

### Traceroute
traceroute TARGET          - UDP (default)

traceroute -T TARGET       - TCP

traceroute -I TARGET       - ICMP

### Telnet (HTTP only, no HTTPS)
telnet TARGET 80           - connect to port 80

### Netcat
nc TARGET PORT             - connect to port

nc -lvnp PORT              - listen on port

## Common Ports
HTTP  = TCP 80

HTTPS = TCP 443

## Key lesson
Web browsing is best active recon method —
hard to distinguish from normal user traffic.
