Projet Docker 1 - Stack Applicative WordPress et MariaDB

L'objectif de ce projet est de mettre en place une stack applicative composée d'une application frontend WordPress et d'une base de données MariaDB, utilisant Docker et Docker Compose

Structure du Projet
Le projet est constitué des fichiers suivants :

docker-compose.yml : Fichier principal de Docker Compose définissant les services et leur configuration.
docker-file.frontend : Dockerfile pour construire l'image personnalisée de WordPress.
docker-file.backend : Dockerfile pour construire l'image personnalisée de la base de données MariaDB.
my.cnf : Fichier de configuration pour MariaDB.

Configuration

docker-compose.yml
Définit deux services : wordpress et db.

Service WordPress
Construit l'image WordPress à partir de docker-file.frontend.
Connecte aux réseaux frontend_network et backend_network.
Montage du volume wordpress_data.
Expose le port 8000.

Service Base de Données (db)
Construit l'image MariaDB à partir de docker-file.backend.
Configuration via des variables d'environnement.
Montage de volumes pour la persistance des données et la configuration.
