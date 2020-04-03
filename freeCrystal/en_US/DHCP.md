Pour que le service de vérification de présence des adresses DHCP fonctionne, il est nécessaire d'installer arp-scan
Dans un terminal :
----
# sudo apt-get install arp-scan  #installation du paquet permetant de scanner le réseaux
# sudo visudo -s
# Ajouter la ligne :
# www-data ALL=NOPASSWD: /usr/bin/arp-scan
----
