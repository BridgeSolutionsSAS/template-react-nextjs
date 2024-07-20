# Usar una imagen base con Node.js
FROM node:20-alpine

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo package.json y package-lock.json
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Cambiar permisos de node_modules
RUN chmod -R 777 node_modules

# Copiar el resto de la aplicación
COPY . .

# Exponer el puerto en el que correrá Vite (por defecto 3000)
EXPOSE 3000

# Comando para iniciar la aplicación en modo desarrollo
CMD ["npm", "run", "dev"]