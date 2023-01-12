# django_tutorial
Tutorial django: https://docs.djangoproject.com/en/3.1/intro/tutorial01/

TAREA_1
Las dependencias necesarias se instalan a traves del comando pip install -r requirements.txt
1. Fork creado(me aprovecho de muchas cosas gracias a este fork)
2. Me voy a aprovechar de que el entorno virtual esta ya creado y asi no hace falta crearlo pero sino se puede mirar eso en el 
gestor_proyect_clientes

3. La base de datos es db.sqlite3, se puede ver el nombre y su configuracion en el archivo django_tutorial/settings.py

4. Las aplicaciones utilizan al menos una tabla de base de datos, por lo que debemos crear las tablas en la base de datos antes de poder usarlas. A través del comando "python manage.py migrate"
        comando-->"python manage.py makemigrations polls"
        Al ejecutar makemigrations, le está diciendo a Django que ha realizado algunos cambios en sus modelos (en este caso, ha realizado otros nuevos) y que desea que los cambios se almacenen como una migración .
        Las migraciones son la forma en que Django almacena los cambios en sus modelos (y, por lo tanto, en el esquema de su base de datos): son archivos en el disco.
5. Para crear un nuevo usuario administrador--> python manage.py createsuperuser
            Usuario de ejemplo--->lorenzo|||||||||||||14052002

La carpeta polls viene generada por "python manage.py startapp polls"(menos static ,templates y urls)


