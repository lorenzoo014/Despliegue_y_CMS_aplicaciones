TAREA_2
1. Se copian los archivos de la anterior carpeta con el entorno virtual ya creado
        Las dependencias las instalo con el comando pip install -r requirements.txt(se le ha añadido la dependencia necesaria)
2. Utilizar MySQL:
                Desde un prompt ejecutado desde el administrador (windows +R-->cmd-->admin) nos vamos hasta el directorio
        mas elemental haciendo uso del "cd ..". Una vez allí ejecutamos cd"ruta" donde tengamos la ruta del mysql y a partir de aquí ya seguimos trabajando con el prompt puesto que no ha surgido problema. Para visualizar un poco mejor este caso se puede hacer uso de la primera imagen
        Para crear un usuario: CREATE DATABASE basedjango;
                                        Es importante que el nombre sea basedjango ya que es el que luego voy a utilizar en settings
        Un usuario: CREATE USER 'usuario'@'localhost' IDENTIFIED BY 'usuario';
                y le damos privilegios para editar la base de datos: GRANT ALL PRIVILEGES ON basedjango.* TO 'usuario'@'localhost';
        







3. La base de datos es db.sqlite3, se puede ver el nombre y su configuracion en el archivo django_tutorial/settings.py

4. Las aplicaciones utilizan al menos una tabla de base de datos, por lo que debemos crear las tablas en la base de datos antes de poder usarlas. A través del comando "python manage.py migrate"
        comando-->"python manage.py makemigrations polls"
        Al ejecutar makemigrations, le está diciendo a Django que ha realizado algunos cambios en sus modelos (en este caso, ha realizado otros nuevos) y que desea que los cambios se almacenen como una migración .
        Las migraciones son la forma en que Django almacena los cambios en sus modelos (y, por lo tanto, en el esquema de su base de datos): son archivos en el disco.
5. Para crear un nuevo usuario administrador--> python manage.py createsuperuser
            Usuario de ejemplo--->lorenzo|||||||||||||14052002

La carpeta polls viene generada por "python manage.py startapp polls"(menos static ,templates y urls)


