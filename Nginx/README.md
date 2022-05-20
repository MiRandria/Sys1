## Installation de Nginx 

### Installation 
Se connecter en tant qu'utilisateur root.

Pour l'installer, exécutez la commande suivante :
    sudo apt-get install nginx

### Configuration 
#####
Pour activer les configurations, il est mieux de créer un lien symbolique vers /etc/nginx/sites-enabled, à l'aide de ces commandes  :
    sudo ln -s /etc/nginx/sites-available/site /etc/nginx/sites-enabled/site

##### Configuration globale de Nginx
Le principal fichier de configuration de Nginx se trouve dans /etc/nginx/nginx.conf.