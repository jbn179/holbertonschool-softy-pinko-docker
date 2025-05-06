# Utiliser la dernière version d'Ubuntu comme image de base
FROM ubuntu:latest

# Mettre à jour APT
RUN apt-get update

# Mettre à niveau les logiciels installés
RUN apt-get upgrade -y

# Installer Python3, pip3 et Flask
RUN apt-get install -y python3 python3-pip

# Gérer le cas d'environnement géré en externe (nécessaire)
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Installer Flask avec pip3
RUN pip3 install flask
RUN pip3 install flask-cors

# Définir le répertoire de travail
WORKDIR /app

# Copier le fichier api.py dans le conteneur
COPY ./api.py /app/api.py

# Exposer le port 5252
EXPOSE 5252

# Exécuter l'application Flask
CMD ["python3", "api.py"]
