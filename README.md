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

``firewall-cmd --parmanent --zone=public --add-port=8000/tcp``

* Then Reload

* Check Infornation add:

``firewall-cmd --list-all``

* Remove Port:

``firewall-cmd --parmanent --zone=public --remove-port=8000/tcp

* firewall ip address add all Access Ip Traffic allow:

``firewall-cmd --parmanent --zone=public --add-source=192.165.13.14`` 
* and Reload

* Rich rule is particular ip address and particular service allow Ex: ssh,http other traffic will be not allow all service block in Firewall: 

``rule family="ipv4" source address="10.0.0.0/24" destination address="192.168.0.10/32" port port="8080-8090" protocol="tcp" accept``

* Here we create a rich rule to reject any traffic that comes from 192.168.0.10/24:

``firewall-cmd --permanent --zone=testing --add-rich-rule='rule family=ipv4 source address=192.168.0.10/24 reject'``

* Rich rules can also be used to rate limit traffic, here we limit incoming SSH connections to 10 per minute:

``firewall-cmd --permanent --add-rich-rule='rule service name=ssh limit value=10/m accept``
 
 
 
