#optimisation de nos container 

- spécification de la  version  de MySQL pour garantir la stabilité et la reproductibilité de mon application `mysql:8.0.`
- nous avons téléchargé le fichier SQL directement depuis GitHub dans le répertoire `docker-entrypoint-initdb.d/ ` pour qu'il soit automatiquement exécuté lors du démarrage du conteneur. Cela simplifie le processus d'initialisation de la base de données.
- nous avons utilise `php:8.0-apache `, pour bénéficier de l'image officielle de PHP avec Apache, ce qui simplifie la configuration de notre serveur web et garantit la compatibilité avec PHP 8.0.
- nous définissons le répertoire de travail comme ` /var/www/html `, ce qui simplifie les instructions ultérieures en évitant de spécifier à chaque fois le chemin complet.
- Nous installons Git pour pouvoir cloner le dépôt depuis `GitHub`
- Nous exécutons Apache avec l'utilisateur `www-data`, ce qui est une bonne pratique pour des raisons de sécurité.
- generation d'un mot de passe robusque 

