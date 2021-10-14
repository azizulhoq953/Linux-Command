# Linux-Command
Command Practice

## Lnux Network System-command

*  Firewall Zone check:

``firewall-cmd --zone-public --list-all``

*Firewall Zone Change:

``firewall-cmd --zone=home --change-interface=eno1``

* firewall active Zone Chack:

``firewall-cmd --get-active-zone``

* Restart Firewall Service :
 
 ``systemctl restart firewalld.service``
 
 * check Restart service working:
 
 
 ``firewall-cmd --get-active-zone``
 
 
