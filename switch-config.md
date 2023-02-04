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
