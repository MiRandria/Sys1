# Installation de Samba 

## Installation 
Se connecter en tant qu'utilisateur root.
 
## Installation du paquet:
##### Commencer par installer le paquet. Exécuter les commandes suivantes pour mettre à jour la liste des paquets et installer Samba.
    apt-get install libcups2 samba samba-common cups

## Déplacer le fichier smb.conf actuel vers smb.conf.bak : 
    mv /etc/samba/smb.conf /etc/samba/smb.conf.bak

## Ensuite créer un nouveau fichier smb.conf : 
    nano /etc/samba/smb.conf

## Avec les contenus suivants :
    [global]
    workgroup = WORKGROUP
    server string = Samba Server %v
    netbios name = debian
    security = user
    map to guest = bad user
    dns proxy = no

## Fermer le fichier de configuration Samba sur le serveur et puis redémarrer Samba :
    systemctl restart smbd.service

