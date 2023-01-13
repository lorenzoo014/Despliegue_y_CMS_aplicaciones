# django_tutorial
Tutorial django: https://docs.djangoproject.com/en/3.1/intro/tutorial01/

<h2>TAREA_1</h2>
Las dependencias necesarias se instalan a traves del comando pip install -r requirements.txt

1. Fork creado(me aprovecho de muchas cosas gracias a este fork)
2. Me voy a aprovechar de que el entorno virtual esta ya creado y asi no hace falta crearlo pero sino se crea a través del siguiente comando: "python -m venv venv"
3. La base de datos es db.sqlite3, se puede ver el nombre y su configuracion en el archivo django_tutorial/settings.py
4. Las aplicaciones utilizan al menos una tabla de base de datos, por lo que debemos crear las tablas en la base de datos antes de poder usarlas. A través del comando "python manage.py migrate"
        comando-->"python manage.py makemigrations polls"
        Al ejecutar makemigrations, le está diciendo a Django que ha realizado algunos cambios en sus modelos (en este caso, ha realizado otros nuevos) y que desea que los cambios se almacenen como una migración .
        Las migraciones son la forma en que Django almacena los cambios en sus modelos (y, por lo tanto, en el esquema de su base de datos): son archivos en el disco.
5. Para crear un nuevo usuario administrador--> python manage.py createsuperuser
            Usuario de ejemplo--->lorenzo|||||||||||||14052002
6. Para probar la aplicación se utiliza el comando --->python manage.py runserver 

La carpeta polls viene generada por "python manage.py startapp polls"(menos static ,templates y urls)

<h2>TAREA_3</h2>

1. Se le cambia el fondo a la aplicacion de encuestas. Para ello:
        Se sigue el directorio polls/templates/polls y se va al archivo index.html donde se comprueba que el directorio "background"
        es el correcto y donde además se le añade como título h2 Lorenzo Martinez Agudo y Raúl Navarro h2". Posteriormente dentro del archivo style.css ubicado en polls/static/polls se cambia el archivo background.jpg por el nuevo que quieras. En mi caso he añadido un archivo.jpg y dentro del archivo style.css el background es el nuevo archivo.jpg
2. Dentro del archivo models.py se crea una nueva clase y se realizan las migraciones con los comandos ya expuestos, que son:
                        python manage.py makemigrations polls
                        python manage.py migrate
3. Se añade el nuevo modelo al sitio de administracion  cambiando el fichero polls/admin.py



