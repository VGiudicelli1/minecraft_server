# config du serveur

## Ajout d'un opérateur

En ligne de commande, sur le conteneur docker

```bash
docker ps # donne l'id du conteneur
docker exec -it <id> /bin/bash

# ajouter un utilisateur en tant qu'opératuer (l'utilisateur doit etre connecté sur le serveur)
rcon-cli op <user> # ex: rcon-cli op Kjegexdes
```

## Création d'un univers

Avec les commandes sur minecraft (avec un compte opérateur)

```bash
/mv create skyblock normal -g IridiumSkyblock
/mv list
```

## Permissions

Avec les commandes sur minecraft

```bash
# création d'un groupe puis ajout des autorisations
/lp creategroup admin
/lp group admin permission set * true

# groupe défault
/lp group default permission set multiverse.access.world true
/lp group default permission set multiverse.access.skyblock true
/lp group default permission set multiverse.teleport.self true
/lp group default permission set multiverse.teleport.others false

# ajouter un user à un groupe
/lp user <pseudo> parent add Admin

```

Nom DNS 

```bash
scutil --get ComputerName
# > MacBook Pro de Vincent
ping macbook-pro-de-vincent.local
```
