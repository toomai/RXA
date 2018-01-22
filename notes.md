# Configuration du SSH sur switch Cisco

https://reussirsonccna.fr/configuration-du-ssh-sur-ios/

U-P: loic:bonjour

 ssh -oKexAlgorithms=+diffie-hellman-group1-sha1

## Accès

username nomUser password XXXX :> Global

line vty 0 4

login username password XXXX

**OU**

login local (Va chercher dans la config globale=> Configurée avec username)

## Bloquer un port

line XX X X

login -> Attends un login

## Ping

De base UNICAST => Si l'hôte se déconnecte on passe en multicast

## Port security
