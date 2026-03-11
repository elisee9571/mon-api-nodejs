![npm badge](https://img.shields.io/badge/npm-v11.9.0-green)
![node badge](https://img.shields.io/badge/node-v25.6.1-green)
![javascript badge](https://img.shields.io/badge/javascript-yellow)

# Mon API nodejs

***

# Table des matières

- [DOCUMENT DE SPÉCIFICATIONS FONCTIONNELLES][1]
- [DOCUMENTATION TECHNIQUE][2]

[1]: ./functional_documentation.md

***

## Description du projet
Il s'agit d'une API REST pour la gestion centralisé d'un forum

## A qui s'adresse ce projet ?
Ce projet est destiné à des devéloppeurs qui souhaite avoir un back qui communique avec differentes plateformes

## Dépendances du projet
```JSON
"dependencies": {
    "bcrypt": "^6.0.0",
    "cross-env": "^10.1.0",
    "dotenv": "^17.3.1",
    "express": "^5.2.1",
    "jsonwebtoken": "^9.0.3",
    "mongodb": "^7.1.0",
    "mongoose": "^9.2.3",
    "morgan": "^1.10.1",
    "nodemon": "^3.1.14",
    "redis": "^5.11.0",
    "sanitize-html": "^2.17.1"
},
"devDependencies": {
    "@eslint/js": "^10.0.1",
    "@faker-js/faker": "^10.3.0",
    "eslint": "^10.0.2",
    "globals": "^17.4.0"
}
```

## Instructions d'utilisation
> Pour commencer à utiliser l'api, vous devez créer un repository en amont sur votre gitbub.

### Installer le projet

1. Cloner le répository
    ```BASH
    git clone https://github.com/elisee9571/mon-api-nodejs.git nom-dossier-projet
    ```

2. Changer le remote
   ```BASH
   cd nom-dossier-projet/
   git add remote origin https://github.com/votre-pseudo/votre-repository.git
   git push -u origin main
   ```

3. Installer les dépendances
   ```BASH
   npm install
   ```

## Configurer
Prérequis : 
> 1. Créer une base de données sur [mongoDB](https://www.mongodb.com)
> 2. Installer redis en local
```BASH
sudo apt install redis
sudo apt install redis-tools
redis-cli
# Vous devriez voir s'afficher
127.0.0.1:6379>
```

Dans votre fichier <code>.env</code> definissez vos variables d'environnement.
```text
NODE_ENV=development
PORT=4000
DATABASE_URL=mongodb+srv://user:!password!@!dns!/?appName=!dbName!
JWT_SECRET=cGFzc3dvcmQ
REDIS_URL=redis://localhost:6379
```

## Exécuter l'API
```BASH
npm run start
```
