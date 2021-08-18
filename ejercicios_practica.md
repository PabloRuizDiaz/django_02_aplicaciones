![Inove banner](/inove.jpg)
Inove Escuela de Código\
info@inove.com.ar\
Web: [Inove](http://inove.com.ar)

---

# Django - Aplicaciones: Ejercicios de práctica.

__Ejercicios basados en las actividades vistas en clase__\

---

1. A partir de lo desarrollado en la clase, ejecute el archivo `docker-compose.yml` para poder correr el contenedor de software.
    OK.. SE GENERO EN LA 2DA TERMINAL
2. Con el contenedor corriendo, ejecute el comando que permite correr la línea de comandos dentro del contenedor.
    OK.. SE EJECUTO 'docker exec -it modulo_2 bash' EN LA TERMINAL 1
3. Dentro del contenedor, instale la librería de django, en su versión 3.2.2.
    OK.. SE EJECUTO pip freeze -> NO TIENE NADA INSTALADO; pip install Django==3.2.2 -> SE INSTALA DJANGO
4. Una vez instalada la librería, debe crear un proyecto de django llamado "modulo_2" en la carpeta del proyecto (`/opt/back_end`).
    OK.. ME DIRIJO A 'cd opt/back_end' (YA QUE ESTABA EN LA RAIZ) PARA CREAR EL PROYECTO DENTRO DE NUESTRA APLICACION.. CREAMOS NUESTRO PROYECTO DJANGO EJECUTANDO 'django-admin startproject modulo_2'
5. Una vez creado el proyecto, debe crear una aplicación en él, llamada "my_app".
    OK.. ME DIRIJO ADENTRO DE MI PROYECTO CREADO (MISMA CARPETA QUE manage.py) Y EJECUTAMOS 'python manage.py startapp mi_app'
6. Generar un directorio para las aplicaciones llamado "applications" a la altura de `manage.py` y debe colocar la carpeta de la aplicación "my_app" dentro de ella, además, tiene que realizar las modificaciones necesarias en el archivo `settings.py` y en `apps.py` para que la aplicación funcione en el proyecto.
    OK.. SE CREO 1RO LA APP EJECUTANDO 'python manage.py startapp mi_app'.. SE CREO LA CARPETA 'apps' Y DENTRO SE MOVIO 'mi_app'.. PARA QUE TODO FUNCIONE, SE MODIFICO 'settings.py' DE 'modulo_2' AGREGANDO EN LA LISTA 'INSTALLED_APPS' EL STRING 'apps.mi_app'.. POR ULTIMO DENTRO DE 'mi_app' SE MODIFICO LA DIRECCION DE 'apps.py' PARA CORREGIR EL DIRECCIONAMIENTO 'apps.mi_app'
7. Generar un archivo ```urls.py``` dentro de la carpeta de la aplicación "my_app" y vincúlelo con el archivo `urls.py` general, ubicado dentro de la carpeta de configuraciones `modulo_2`.
    OK.. SE CREO EL FILE 'urls.py' DENTRO DE APPS.MI_APP, AHI SE IMPORTARON LAS LIBRERIAS NECESARIAS.. SE CREO LA VARIABLE 'urlpatterns' DONDE SE IRAN AGREGANDO LOS URLS CORRESPONDIENTES DE APPS.. POR ULTIMO SE INFORMA AL PROYECTO EN 'urls.py' INCLUIRLE LA RUTA DE URLS INCLUYENDO 'path('apps/mi_app/', include('apps.mi_app.urls'))'
---
## Recuerde
* Los comandos necesarios para cada paso se encuentran en el archivo README.md
* La explicación de cada paso puede ser revisada tanto en el video de la clase como en el documento de clase del presente módulo, también puede solicitar ayuda en el foro correspondiente.
* Para acceder al servidor en el navegador, debe introducir la dirección `localhost:8000`
