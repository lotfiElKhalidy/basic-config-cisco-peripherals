# Configuration des paramètres de base d'un switch

## Configuration duc commutateur SVI

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

> 2. Configurer la passerelle par défaut
- Configurer la passerelle par défaut pour le commutateur.
```
$ S1(config)# ip default-gateway address
```

> 3. Vérifier la configuration
```
$ S1# show ip interface brief
$ S1# show ipv6 interface brief
```

> 4. Sécuriser Telnet à distance / accès SSH

```
$ Router(config-line)# line vty 0 4
$ Router(config-line)# password password
$ Router(config-line)# login
$ Router(config-line)# transport input {ssh | telnet}
```


> 5. Sécuriser tous les mots de passe dans le fichier de configuration.

```
$ Router(config)# service password-encryption
```

> 6. Fournir un avertissement légal

```
$ Router(config)# banner motd #message d'avertissement#
```

> 7. Enregistrer la configuration.

```
$ Router# copy running-config startup-config
```

## Configuration des intrefaces

> 1. Configuration des interfaces des routeurs
```
$ Router(config)# interface type number (e.g interface gigabitEthernet 0/0/1)
$ Router(config-if)# ip address ipv4-address subnet-mask (e.g ip address 192.168.10.15 255.255.255.0)
$ Router(config-if)# ipv6 address ipv6-address/prefix-length (e.g ipv6 address 2001:db8:feed:224::1/64)
$ Router(config-if)# no shutdown
```

> 2. Vérifier la configuration d'une interface
```
$ Router# show ip interface brief
$ Router# show ipv6 interface brief
```

> 3. Configuration de la passerelle par défaut
```
$ Router# ip default-gateway ipv4-address
```
