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
