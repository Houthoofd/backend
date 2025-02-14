# Utiliser une image Node.js officielle légère (alpine)
FROM node:18-alpine

# Définir le répertoire de travail
WORKDIR /app

# Copier uniquement les fichiers package.json et package-lock.json pour optimiser le cache Docker
COPY api/package*.json ./

# Installer les dépendances (utiliser --only=production pour installer uniquement celles nécessaires en prod)
RUN npm install --only=production

# Copier le reste des fichiers sources de l'application backend
COPY api/ .

# Exposer le port utilisé par votre API backend
EXPOSE 5000

# Démarrer l'API
CMD ["npm", "start"]

