## Enueration

### NetBIOS
* `nbtstat` is a Windows tool for enumeration of NetBIOS-based shares on DOS and Windows machines.
* `nbtstat -a [ip]` will find all Windows shares on a target machine.
* `nbtstat -c` will show the NetBIOS cache.
* `net use` will establish the available network shares.
* `nbstat.nse` on nmap will enumerate NetBIOS shares.

### SNMP
Port 161
* `nmap -sU` required because it relies on UDP.
* `snmp-sysdescr.nse` on nmap will enumerate SNMP information.
* `snmp-processes.nse` to get running processes on the specific device(s).
* `snmp-check` command also to get running processes on the specific device(s).
* `snmp-interfaces.nse` to the detected network interfaces on the specific device(s).
  
### SMB
Port 445
* `smb-enum-shares` on nmap will retun network shares for Windows.
* `smb-enum-users` on nmap will retun network users for Windows.
* `smb-enum-groups` on nmap will retun network workgroups for Windows.
* `smbclient` is a Linux tool to access Windows shares.

### LDAP
Port 389
* `ldap-brute.nse` on nmap will enumerate LDAP information.

### NFS
Port 2049
* `nfs-ls.nse` on nmap with enumerate NFS shares.

### SMTP
Port 25
* `smtp-enum-users.nse` on nmap to enumerate SMTP users

### RDP
Port 3389
* `rdp-enum-encryption` on nmap to determine encryption levels.
*  `rdp-scanner` available in metasploit to get possible exploits.
*  `rdesktop` or `xfreerdp` to connect to remote desktop from Linux.
*  `rdp-check` from Impacket to check if valid credentials.
