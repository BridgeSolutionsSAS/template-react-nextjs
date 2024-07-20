# Establece la imagen base
FROM node:20-alpine AS builder

# Establece el directorio de trabajo
WORKDIR /app

# Copia el package.json y el package-lock.json al directorio de trabajo
COPY package.json ./
COPY package-lock.json ./

# Instala las dependencias
RUN npm install

# Copia el resto del código de la aplicación al directorio de trabajo
COPY . .

# Construye la aplicación Next.js
RUN npm run build

# Expone el puerto 8080
EXPOSE 8080

# Comando para iniciar la aplicación
CMD ["npm", "start","--", "-p", "80"]
