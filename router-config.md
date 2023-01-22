# Configuration des paramètres de base d'un routeur

## Configuration des paramètres initiaux du routeur

> 1. Configurer le nom de l'appareil
```
$ Router(config)# hostname newName
```

> 2. Sécuriser le mode d'exécution privilégié.
```
$ Router(config)# enable secret newPassword
```

> 3. Sécuriser le mode d'exécution utilisateur
```
$ Router(config)# line console 0
$ Router(config-line)# password password
$ Router(config-line)# login
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



