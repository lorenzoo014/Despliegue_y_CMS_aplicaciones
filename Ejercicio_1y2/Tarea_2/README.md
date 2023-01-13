<h2>TAREA_2</h2>
1. Se copian los archivos de la anterior carpeta con el entorno virtual ya creado
        Las dependencias las instalo con el comando pip install -r requirements.txt(se le ha añadido la dependencia necesaria)
2. Utilizar MySQL:
                Desde un prompt ejecutado desde el administrador (windows +R-->cmd-->admin) nos vamos hasta el directorio
        mas elemental haciendo uso del "cd ..". Una vez allí ejecutamos cd"ruta" donde tengamos la ruta del mysql y a partir de aquí ya seguimos trabajando con el prompt debido a que no ha surgido problema. Para visualizar un poco mejor este caso se puede hacer uso de la primera imagen.
3. Para crear un usuario: create database basedjango;
                                He establecido el nombre como basedjango ya que es el que luego voy a utilizar en settings
4. Vas a crear esta cuenta, establecer una contraseña y otorgar acceso a la base de datos que creaste. Primero, cree el usuario y configure su contraseña escribiendo el siguiente comando. Recuerde elegir una contraseña segura para su base de datos reemplazando passworden este ejemplo:
                Comando-->CREATE USER 'djangouser'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
        Informe a la base de datos que djangouser debe tener acceso completo a la base de datos que configuró:
                Comando-->GRANT ALL ON blog_data.* TO 'djangouser'@'localhost';
5. Las aplicaciones utilizan al menos una tabla de base de datos, por lo que debemos crear las tablas en la base de datos antes de poder usarlas. A través del comando "python manage.py migrate"
6. Para crear un nuevo usuario administrador--> python manage.py createsuperuser
            Usuario de ejemplo--->lorenzo|||||||||||||14052002
7. Para configurar nginx como proxy inverso para servir la aplicación sólo he podido averiguar cómo hacerlo en linux los comandos serían los siguientes:
        **En el archivo  EXPLICACIONES_2.2.md se encuentra este paso**
8. Dentro del archivo settings.py cambio "DEBUG=True" por "DEBUG=False" para que los errores de ejecución no den información sensible de la aplicación.
