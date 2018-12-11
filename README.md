Para instalar la apliacacion en modo desarrollo debera seguir los siguientes pasos:

1-) Instalar el controlador de versiones git:
---------------------------------------------
    
    $ su

    # aptitude install git

2-) Descargar el codigo fuente del proyecto IVSS_STV:
-------------------------------------------------------

    Para descargar el código fuente del proyecto contenido en su repositorio GIT realice un clon del proyecto, con el siguiente comando:

    $ git clone git@github.com:conan4069/control_estudio_django.git
                
3-) Instalar Dependencias:
------------------------------
    # aptitude install python3.5 python3-pip python3-dev python3-setuptools

    Para el uso es recomendable usar entornos virtuales los dos modos son:

3.1-) Virtualenvwrapper Modo
----------------------------

    # aptitude install python3-virtualenv virtualenvwrapper

    Salir del modo root y crear el ambiente:

    $ mkvirtualenv --python=/usr/bin/python3 school

    Para activar el ambiente virtual school ejecute el siguiente comando:

    $ workon school

3.1.1-) Virtualenv modo
----------------------------

    # aptitude install virtualenv

    mkdir entornos_virtuales

Desde el terminal, moverse a la carpeta entornos_virtuales y ejecutar

    $ cd entornos_virtuales/

    $ virtualenv -p python3 school

Para activar el entorno

    $ source school/bin/activate

4-) Instalar dependencias en el entorno virtual:
------------------------------------------------
    Una vez iniciado el entorno virtual no desplazaremos a la carpeta del projecto
    (school) $ cd directorio-elegido/control_estudio_django/requeriments

    (school) $ pip install -r base.txt
    
    Una vez instalada las dependencias del entorno virtual nos debemos desplazar a la base del proyecto para seguir con el resto de los pasos

    (school)$ cd ../administratorSchool

5-) Migrar los modelos:
-----------------------

    (school)$ python manage.py makemigrations

    (school)$ python manage.py migrate

6-) Iniciar la aplicacion:
--------------------------

    (school)$ python manage.py runserver