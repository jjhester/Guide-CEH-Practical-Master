# Scanning Commands
## NMAP
### Common Commands
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
|`sudo nmap -sN 10.10.12.9`| TCP Null|
|`sudo nmap -sF 10.10.12.9`| TCP FIN |
|`sudo nmap -sX 10.10.12.9`| TCP XMas|
|`sudo nmap -sM 10.10.12.9`| TCP Maimon|
|`sudo nmap -sA 10.10.12.9`| TCP ACK (Firewall)|
|`sudo nmap -sW 10.10.12.9`| TCP Window (Firewall)|
### Additional Switches
| Switch | Effect|
|--------|-------|
|`-p-`| All port scan (beyond standard)|
|`-sV`| Service versioning|
|`-sC`| Service versioning with safe scripts|
