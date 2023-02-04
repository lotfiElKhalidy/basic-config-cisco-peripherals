# Configuration des paramètres de base d'un switch

## Configuration du commutateur SVI

> 1. Configurer l'interface de gestion
- Passer en mode de configuration d'interface pour SVI.
```
$ S1(config)# interface vlan 99
```
- Configurer l'adresse IPv4 de l'interface de gestion.
```
$ S1(config-if)# ip address ipv4-address mask
```
- Configurer l'adresse IPv6 de l'interface de gestion.
```
$ S1(config-if)# ipv6 address ipv6-address/prefix
```
- Activer l'interface de gestion
```
$ S1(config-if)# no shutdown
```
- Repasser en mode d'exécution privilégié
```
$ S1(config-if)# end
```
- Enregistrer la configuration en cours dans la configuration de démarrage.
```
$ S1# copy running-config startup-config
```

## Configuration des ports de commutateur

> 1. Configurer l'interface de gestion
- Passer en mode de configuration d'interface.
```
$ S1(config)# interface FastEthernet 0/1
```
- Configurer le mode bidirectionnel d'interface.
```
$ S1(config-if)# duplex full
```
- Configurer la vitesse d'interface
```
$ S1(config-if)# speed 100
```
- Activer l'interface de gestion
```
$ S1(config-if)# no shutdown
```
- Repasser en mode d'exécution privilégié
```
$ S1(config-if)# end
```
- Enregistrer la configuration en cours dans la configuration de démarrage.
```
$ S1# copy running-config startup-config
```

## Commandes de vérification des commutateurs

- Activer l'auto-MDIX
- Lorsque la fonction auto-MDIX est activée, l'interface détecte automatiquement le type de connexion de câble requis (droit ou croisé) et configure la connexion de manière appropriée
```
$ S1(config-if)# mdix auto
```
- Examiner le paramètre Auto-MDIX pour une interface spécifique
```
$ S1# show controllers ethernet-controller interface_name phy | include MDIX
```
- Afficher l'état et la configuration des interfaces.
```
$ S1# show interfaces [interface-id]
```
- Afficher la configuration initiale actuelle.
```
$ S1# show startup-config
```	
- Afficher la configuration courante.
```
$ S1# show running-config
```
- Afficher les informations sur le système de fichiers Flash.
```
$ S1# show flash
```
- Afficher l'état matériel et logiciel du système.
```
$ S1# show version
```
- Afficher l'historique de la commande saisie.
```
$ S1# show history
```
- Afficher les informations IP d'une interface.
```
$ S1# show ip interface [interface-id] OU S1# show ipv6 interface [interface-id]
```
- Afficher la table d'adresses MAC.	
```
$ S1# show mac-address-table OU S1# show mac address-table
```
