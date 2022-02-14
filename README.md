# Deploy a Heroku

## Objeto del documento

Describir el proceso para deplegar a producción en [Heroku](https://www.heroku.com/) + [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) una aplicación de [ExpressJS](https://expressjs.com/).

## Objetivo del deploy

**Base de datos**: hacer el paso a producción de la base de datos local a una base de datos remota en MongoDB Atlas:
  1. Realizar el registro en MongoDB Atlas y crear la base de datos remota (stage 1)
  
**Servidor**: hacer el paso a producción de la aplicación de servidor local a una aplicación remota en Heroku:
  1. Realizar el registro en Heroku y crear la aplicación remota (stage 3)
  2. Transferir los archivos de la aplicación local a la aplicaciónn remota (stage 4)


## Fases de paso a producción

- Stage 1: [Deploy de la Base de Datos a MongoDB Atlas](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage1.md)
- Stage 3: [Registro en Heroku y creación de aplicación para servidor](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage3.md)
- Stage 4: [Paso a producción: servidor](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage4.md)
