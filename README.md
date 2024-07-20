# NextJs + Docker

Este repositorio es un ejemplo de como startear un proyecto NextJs para el ambiente de desarrollo y productivo.

# Pre-requisitos

- Docker y docker-compose.
- Node.Js y npm (Desarrollo)

# Start the app (Desarrollo)

```bash
# Instalar los paquetes externos
npm install

# Levantar imagen de docker
npm run image:dev
```

# Build the app (Produccion)

```bash
docker-compose -f devops/production/docker-compose.yml up --build
```
