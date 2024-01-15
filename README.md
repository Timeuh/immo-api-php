
Slim 4 API
Ce projet "Slim 4 API" consiste en une API simple utilisant Slim v4 avec MySQL. L'application est destinée à être utilisée avec Docker Compose pour une mise en place facile.

### 1. Cloner le dépôt :

Clonner le dépôt GitHub suivant dans le répertoire de votre choix :
```git
   git clone https://github.com/Timeuh/immo-api-php.git
```

### 2. Installation :

Veuillez executer la commande ci-dessous pour installer les dépendances PHP nécessaires.
```bash
composer install
```

### 3. Configuration :
Assurez-vous de remplir les informations nécessaires dans un fichier que vous allez créer et qui s'appelera .env à la racine du projet pour configurer le projet. Les variables à remplir sont les suivantes :

```dotenv
MYSQL_HOST=
MYSQL_DATABASE=
MYSQL_USER=
MYSQL_PASSWORD=
MYSQL_ROOT_PASSWORD=
```

De plus, ajoutez les données nécessaires à la base de données en plaçant les fichiers dans le dossier db-data dans votre base de données sur adminer.

### 4. Lancer les conteneurs

Lors du premier lancement avec Docker Compose, suivez ces étapes pour installer et exécuter l'application. À l'aide d'un terminal placez vous à la racine de votre projet pour executer les commandes suivantes :

Lancez le conteneur du service PHP :

```bash
docker-compose up -d immo-php
```
Lancez le conteneur du service de la base de données :

```bash
docker-compose up -d immo-db
```
Lancez le conteneur du service d'administration des bases SQL :

```bash
docker-compose up -d adminer
```
L'application sera accessible à l'adresse ci-dessous ou au port que vous avez spécifié dans le fichier .env.
```http request
http://localhost:2080
```

Pour acceder à la base données, il vous suffit de vous connecter à cette adresse : 
```http request
http://localhost:8080
```
Ensuite mettez les informations nécessaires pour vous connecter.
