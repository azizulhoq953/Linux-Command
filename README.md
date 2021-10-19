# Linux-Command
Command Practice

## Linux Network System-command

*  Firewall Zone check:

``firewall-cmd --zone-public --list-all``

* Firewall Zone Change:

``firewall-cmd --zone=home --change-interface=eno1``

* firewall active Zone Chack:

``firewall-cmd --get-active-zone``

* Restart Firewall Service :

 ``systemctl restart firewalld.service``
 
 * check Restart service working:
 
 ``firewall-cmd --get-active-zone``
 
 * firewall default zone set:
 
 ``firewall-cmd --set-default-zone=home``
 
 * Firewall all service show:
 
 ``firewall-cmd --get-services``
 
 * public zone http service add then Ensure Must be Reload:
 
 ``firewall-cmd --parmanent --zone=public --add-service=http``
 
 * http Service Remove:
 
 ``firewall-cmd --parmanent --zone=public --remove-service=http``
 
* Firewall Run status check:

``systemctl status firewalld.service``

* First Time Firewall Run Good Practice Enable System:

``systemctl enable firewalld``

* and Then service Start:

``systemctl start firewalld``

* Firewall Port Add:

``firewall-cmd --parmanent --zone=public --add-port=8000``

 
 
 
