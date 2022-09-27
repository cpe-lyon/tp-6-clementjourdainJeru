# Exercice 1


# Exercice 2

1.  kjhgr
2.  Il s'agit du loopback, qui est une interface virtuelle d'un matériel réseau (ou d'un ordinateur), et par extension une adresse associée à cette interface. Ainsi, quand il la contacte il "boucle" sur lui-même. 
3.  sudo apt purge init
4.  hostnamectl set-hostname serveur.tpadmin.local

# Exercice 3.
1.  sudo apt install isc-dhcp-server
2.  sudo nano /etc/netplan/00-uhgoiu avec comme modification addresses: - 192.168.100.1 ; puis sudo netplan apply puis ping
3.  Il s'agit du temps où le serveur dhcp loue une adresse ip à un poste.
4.  sudo nano /etc/default/isc-dhcp-server puis interfacev4="enp0s8"
5.  sudo systemctl restart isc-dhcp-server puis sudo systemctl status isc-dhcp-server, c'est arqué actif
6.  Client configuré
7.  DHCPDISCOVER signifie que le serveur reçoit une demande d'adresse IP en indiquant l'adresse mac de la machine qui le demande, DHCPPOFFER soumet une adresse IP au client, DHCPREQUEST valide l'adresse IP choisie et enfin le serveur répond simplement par un DHCPACK avec l’adresse IP pour confirmation de l’attribution. L'adresse choisie étant `192.168.100.100`, elle se situe bien dans la plage spécifiée.
8.  Le fichier `/var/lib/dhcp/dhcpd.leases`contient toutes les llocation d'adresses IP, tandis que `dhcp-lease-list` liste les locations IP actuelles avec l'adresse MAC du la machine client et la durée d'attribution de l'adresse IP
9.  
