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
EXPOSE 3001

# Définir les variables d'environnement nécessaires
ENV DB_USER=root
ENV DB_PASSWORD=rootpassword
ENV DB_NAME=customerdb
ENV DB_HOST=customer-database
ENV MESSAGE_BUS_USERNAME=user
ENV MESSAGE_BUS_PASSWORD=password
ENV MESSAGE_BUS=rabbitmq
ENV MESSAGE_BUS_TIMEOUT=5000
ENV SERVICE_NAME=customer-service
ENV PORT=3001

# Commande pour démarrer l'application
CMD ["sh", "-c", "npx sequelize-cli db:migrate && node ./bin/www"]
