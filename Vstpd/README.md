# Installation de Vstpd 

## Installation 
Se connecter en tant qu'utilisateur root.

## Installation du paquet :
Commencer par installer le paquet. Exécuter les commandes suivantes pour mettre à jour la liste des paquets et installer vsFTPd.
    apt-get update
    apt-get install vsftpd

## Configuration de vsFTPd :
Faire une sauvegarde du fichier de configuration original avec 
    cp /etc/vsftpd.conf /etc/vsftpd.conf.backup 

Ouvrir le fichier de configuration en utilisant 
    nano /etc/vsftpd.conf 

Créer un dossier ftp dans le répertoire personnel
    mkdir /home/ftpuser/ftp

Supprimez les droits d'écriture du dossier personnel de l'utilisateur 
    chmod a-w /home/ftpuser

Attribuez la propriété du dossier ftp à l'utilisateur    
    ftpuser /home/ftpuser/ftp

## Redémarrez le service vsftpd : 
    /etc/init.d/vsftpd restart




