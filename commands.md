# Scanning Commands
## NMAP
| Commmand | Scan Type|
|----------|----------|
|`sudo nmap -PR -sn 10.10.12.13/29`| ARP|
|`sudo nmap -PE -sn 10.10.12.13/29`| ICMP Echo|
|`sudo nmap -PP -sn 10.10.12.13/29`| ICMP Timestamp|
|`sudo nmap -PM -sn 10.10.12.13/29`| ICMP Address Mask|
|`sudo nmap -PS22,80,443 -sn 10.10.12.13/29`| TCP SYN Ping|
|`sudo nmap -PA22,80,443 -sn 10.10.12.13/29`| TCP ACK Ping|
|`sudo nmap -PU53,161,162 -sn 10.10.12.13/29`| UDP Ping|
|`nmap -sT 10.10.12.9`| TCP Connect (3-Way)|
|`nmap -sS 10.10.12.9`| TCP SYN (RST)|
|`nmap -sU 10.10.12.9`| UDP|
