# Deploy a Heroku

## Objeto del documento

Describir el proceso para deplegar a producción en [Heroku](https://www.heroku.com/) + [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) una aplicación de [ExpressJS](https://expressjs.com/).

## Especificaciones

El deploy se realizará en base a los siguientes objetivos:

- Hacer el paso a producción de la base de datos local a una base de datos remota en MongoDB Atlas:
  1. Crear una base de datos remota en MongoDB Atlas (stage 1).
  2. Exportar los datos de la base de datos local e importaros en la base de datos remota (stage 2)
- Hacer el paso a producción de la aplicación de servidor local a una aplicación en Heroku:
  1. Realizar el registro en Heroku y crear la aplicación remota (stage 3)
  2. Transferir los archivos de la aplicación local a la aplicaciónn remota (stage 4)


## Fases de paso a producción

1. [Registro en MongoDB Atlas y configuración base](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage1.md)
2. [Paso a producción: base de datos](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage3.md)
3. [Registro en Heroku y creación de aplicación para servidor](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage2.md)
4. [Paso a producción: servidor](https://github.com/german-alvarez-dev/deploy-express-app/blob/main/stage4.md)
