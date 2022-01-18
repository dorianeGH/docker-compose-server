# Dockerfile
FROM node:lts-alpine

# Ici on va avoir besoin des fichiers source de l'application mais aussi des paquets du dossier node_modules.
# Pour cela on va d'abord copier les fichiers package.json et package-lock.json, puis on va faire exécuter npm i.
# Enfin on copie les fichiers du dossier src

RUN mkdir /app
WORKDIR /app
COPY package*.json ./
RUN npm i
COPY src src

CMD npm run dev