#TP2

## Q1

Le switch envoie sur un seul port (celui associé à la MAC adresse) mais si l'hôte se déconnecte,  il flood sur tous les ports anycast > broadcast et envoie une requete arp.

Si deux hôtes ont la même MAC, la table change à chaque nouvelle requête ARP selon le premier à lui répondre.

Un switch retient toute la table de switching. Si un switch est branché sur un port il associe plusieurs MAC adresse sur le même port. D'abord l'adresse MAC du switch en lui même et ensuite tous les hôtes branchés sur celui-ci.

show mac-address-table: show arp table
clear mac-address-table {Dynamic/Static/secure}
port-security {max-con} **nbreaddresse**

Il y a plusieurs type de sécurité sur un port: 
- De base il bloque juste les trames si une adresse mac différente est détectée
- Sinon il y a moyen que le port se ferme complètement

Le switch associe une MAC à un port de façon définitive, si on change le host de port, ça ne fonctionne pas
