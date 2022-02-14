
# Deploy de la Base de Datos a MongoDB Atlas

MongoDB Atlas ofrece un servicio gratuito para alojar bases de datos en remoto, pudiendo accederlas a través de un string de conexión que sustituirá a tu actual `mongodb://localhost/db_local`

## Registro y selección de Cluster

1. Acceder a [MongoDB Atlas](https://account.mongodb.com/account/register) y realizar el proceso de registro con los datos personales y las preguntas que saldrán tras la verificación del email.<br/><br/>
2. Elige el Cluster SHARED (gratuito). Selecciona *CREATE*: 
  <img width="940" alt="Captura de pantalla 2022-02-14 a las 10 13 43" src="https://user-images.githubusercontent.com/46670724/153834660-6cb2397c-0d1a-4efe-ba6e-e1b2e9cb044f.png"><br/><br/>
3. En la siguiente pantalla, mantener AWS y seleccionar un servidor europeo. Seleccionar *Create Cluster*: <img width="1140" alt="Captura de pantalla 2022-02-14 a las 10 19 05" src="https://user-images.githubusercontent.com/46670724/153835435-e67c7cfe-6b2d-4d95-aa58-b1e2f8fffb51.png">
<br/><br/>
4. Para terminar, elegir *SKIP* en la pantalla de invitaciones al servicio:
   <img width="891" alt="Captura de pantalla 2022-02-14 a las 10 22 07" src="https://user-images.githubusercontent.com/46670724/153835923-2bd51e3b-87cf-4b5c-9468-5144cba6c29f.png">


## Configuración de Cluster

5. En la pantalla de **Security Quickstart**, seleccionar **Username and Password** como método de autenticación, y rellenar el `username` y `password` deseados del formulario inferior. Selecciomnar **Create user**.
  <img width="933" alt="Captura de pantalla 2022-02-14 a las 10 24 43" src="https://user-images.githubusercontent.com/46670724/153836351-0cead578-c95a-4723-8c8d-e1bf97698a3a.png"><br/><br/>
6. En la sección de modo de conexión, seleccionar la opción **My local environment** e incluir el valor `0.0.0.0/0` en la sección **IP Address**, lo que permitirá acceder la BBDD desde cualquier IP:
  <img width="933" alt="Captura de pantalla 2022-02-14 a las 10 29 25" src="https://user-images.githubusercontent.com/46670724/153837294-39b5953c-3feb-40f3-be8b-5c41c93e32f2.png">
<br/><br/>
7. Click en _Add entry_ y en _Finish and close_.

## Obtención del string de conexión
8. En el panel del Cluster, hacer click en el botón *Connect*:
  <img width="1201" alt="Captura de pantalla 2022-02-14 a las 10 32 35" src="https://user-images.githubusercontent.com/46670724/153839026-d118427d-ce83-46aa-b738-83835e5d416d.png"> <br/><br/>
9. En la ventana modal, seleccionar *Connect using MongoDB Compass* entre los diferentes métodos de conexión:
  <img width="1201" alt="Captura de pantalla 2022-02-14 a las 10 34 35" src="https://user-images.githubusercontent.com/46670724/153838033-7a3590c2-4367-44f9-9201-351530ab6a8f.png"><br/><br/>
10. Seleccionar *I have mongo Compass*, copiar el string de conexión inferior y modificarlo de la siguiente forma:
    - Sustituir `<password>` por la contraseña de conexión.
    - Sustituir `/test` por el nombre deseado para la base de datos.
    <img width="1201" alt="Captura de pantalla 2022-02-14 a las 10 35 54" src="https://user-images.githubusercontent.com/46670724/153838238-210a76cf-03d2-4afc-85d1-b02f2bc22d5e.png"><br/><br/>
    
## Integración del string de conexión
11. Ya puedes conectarte a tu BBDD remota pegando el string de conexión en dos lugares:
    - Para Mongo Compass, pegarlo en la pantalla inicial de conexión. Estarás conectado a tu BBDD remota, contra la que podrás operar con normalidad tal y como lo hacías en local.
    - Para una conexión mediante Mongoose, pegarlo como string de conexión en el archivo `.env` para que sea utilizado en `mongoose.connect()`. Estarás trabajando contra tu BBDD remota, tal y como lo hacías con la BBDD local.

