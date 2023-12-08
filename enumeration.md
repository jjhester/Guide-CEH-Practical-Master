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

### LDAP
Port 389
* `ldap-brute.nse` on nmap will enumerate LDAP information.

### NFS
Port 2049
* `nfs-ls.nse` on nmap with enumerate NFS shares.

### SMTP
Port 25
* `smtp-enum-users.nse` on nmap to enumerate SMTP users

