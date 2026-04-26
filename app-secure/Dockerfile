# Dockerfile minimal pour node-app-secure 
FROM node:20-alpine3.22 
# Mettre à jour le système 
RUN apk update && apk upgrade --no-cache
# Définir le dossier de travail 
WORKDIR /app 
# Copier uniquement package.json pour installer les dépendances 
COPY package.json ./ 
# Installer les dépendances de production 
RUN npm install --production 
# Copier le fichier principal de l'application 
COPY app.js ./ 
 
# Exposer le port de l'application 
EXPOSE 3000 
# Commande pour lancer l'application 
CMD ["node", "app.js"]
