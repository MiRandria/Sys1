# Installation de Nfs 

## Installation 
Se connecter en tant qu'utilisateur root.

## Installation des paquets :
##### L'installation se fait par deux paquets. Exécuter les commandes suivantes pour mettre à jour la liste des paquets et installer Nfs.
    yum install nfs-utils nfs-utils-lib

##### Activer au passage les services rpcbind et nfs au démarrage du système et on les démarre :
    systemctl enable --now rpcbind
    systemctl enable --now nfs

## Configuration 
### Partie client
##### Pour la partie cliente, on installe aussi les paquets : 
    yum install nfs-utils nfs-utils-lib

##### Monter le partage :
    mkdir -p /media/nfs
    mount -t nfs4 192.168.21.200:/media/partage /media/nfs

##### Avec la commande df, on peut voir que tout est monté :
    df -h

On peut aussi monter ça dans le fstab.