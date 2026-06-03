# THM - Nmap Port Scanning

## Port States

* **open** – the port is actively listening for connections
* **closed** – the port is reachable, but no service is running (typically responds with RST)
* **filtered** – Nmap cannot determine if the port is open or closed due to filtering (firewall/ACL)
* **unfiltered** – the port is reachable, but Nmap cannot determine if it is open or closed (common in ACK scans)
* **open|filtered** – no response received; could be open or filtered (common in UDP scans)
* **closed|filtered** – Nmap cannot distinguish between closed and filtered (rare, scan-specific cases)

Key idea:

* **closed ≠ unreachable** → it means the host responded, but no service is listening.

## Key Scan Types

* **-sS (SYN scan)**
  Half-open scan (SYN scan)
  Fast and stealthy, requires root/administrator privileges

* **-sT (TCP connect scan)**
  Full TCP handshake using the operating system’s networking stack

* **-sU (UDP scan)**
  Slower and less reliable due to frequent lack of responses

* **-sA (ACK scan)**
  Used mainly for firewall mapping, not service detection

* **-sN / -sF / -sX (NULL / FIN / Xmas scans)**
  Stealth scans exploiting TCP stack behavior

## Key Options

* **-p-** → scan all 65535 ports
* **-p 80,443** → scan specific ports
* **-F** → fast scan (top 100 ports instead of default ~1000)
* **-r** → scan ports sequentially
* **-T0 – T5** → timing templates (T0 slowest, T5 fastest/aggressive)

Additional useful options:

* **-sV** → service version detection
* **-O** → OS detection
* **-A** → aggressive scan (OS + version + scripts + traceroute)
* **-Pn** → skip host discovery (assume host is up)

## TCP Flags

* **SYN** → initiates a connection
* **ACK** → acknowledges received data
* **SYN+ACK** → server response to SYN
* **FIN** → graceful connection termination
* **RST** → connection reset (port closed or rejected)
* **PSH** → push data immediately to application layer
* **URG** → urgent data flag (rarely used in practice)

## Key takeaway

Nmap interpretation logic in practice:

* **No response** → filtered or UDP behavior
* **RST response** → port closed
* **SYN+ACK response** → port open
* **ICMP unreachable** → often filtering (especially for UDP scans)
