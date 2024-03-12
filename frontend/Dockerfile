# Utiliser une image PHP avec Apache
FROM php:8.0-apache

# Activer le module Apache mod_rewrite
RUN a2enmod rewrite

# Définir le répertoire de travail dans le conteneur
WORKDIR /var/www/html
#Installation du pilote PDO 
RUN docker-php-ext-install pdo pdo_mysql
#clone 
RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/michelnyobe/frontend_debops.git

# Copier les fichiers PHP dans le conteneur
RUN mv frontend_debops/*  /var/www/html/

# Exposer le port 80 pour accéder à l'application PHP via le navigateur
EXPOSE 80

# Commande pour démarrer Apache lors du lancement du conteneur
CMD ["apache2-foreground"]
