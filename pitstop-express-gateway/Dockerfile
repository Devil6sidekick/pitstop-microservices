# Utiliser une image de base officielle Node.js
FROM node:14

# Définir le répertoire de travail
WORKDIR /usr/src/app

# Copier package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier le reste de l'application
COPY . .

# Exposer le port utilisé par l'application
EXPOSE 8080

# Commande pour démarrer l'application
CMD ["node", "server.js"]
