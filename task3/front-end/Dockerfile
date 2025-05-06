# Utiliser la dernière version de Nginx comme image de base
FROM nginx:latest

# Copier les fichiers du front-end dans le répertoire approprié de Nginx
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier le fichier de configuration Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

