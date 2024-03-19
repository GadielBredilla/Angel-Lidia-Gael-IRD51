# Tema 15: Creación de un Proyecto Django y Desarrollo de una Aplicación

En este tema, se describen los pasos fundamentales para crear un proyecto Django, configurar la base de datos, definir modelos, crear aplicaciones y desarrollar una vista básica que integra JavaScript en una plantilla. A continuación, se presentan los pasos detallados junto con los códigos de ejemplo:

1. **Instalación de Herramientas:**
   - Descargar e instalar Laragon para el entorno de desarrollo local.
   - Elegir un editor de código (por ejemplo, Sublime Text).

2. **Creación del Proyecto Django:**
   ```bash
   django-admin startproject mysite
   ```

3. **Creación de Aplicaciones:**
   ```bash
   cd mysite
   python manage.py startapp webapp
   ```

4. **Configuración de Base de Datos y Modelos:**
   - En el archivo `settings.py`:
     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.postgresql',
             'NAME': 'sap_db',
             'USER': 'postgres',
             'PASSWORD': '12345',
             'HOST': 'localhost',
             'PORT': '5432',
         }
     }
     ```
   - En el archivo `models.py` dentro de la aplicación `webapp`:
     ```python
     from django.db import models

     class Persona(models.Model):
         nombre = models.CharField(max_length=255)
         apellido = models.CharField(max_length=255)
         email = models.CharField(max_length=255)

         def __str__(self):
             return f'Persona: {self.nombre} {self.apellido} {self.email}'
     ```

5. **Migraciones y Creación de Superusuario:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   python manage.py createsuperuser
   ```

6. **Desarrollo de la Vista:**
   - En el archivo `views.py` dentro de la aplicación `webapp`:
     ```python
     from django.shortcuts import render

     def javascript_request(request):
         return render(request, 'webapp/javascript_request.html')
     ```
   
7. **Configuración de Carpetas y Archivos Estáticos y de Plantillas:**
   - Crear una carpeta llamada `templates` en la aplicación `webapp`.
   - Crear un archivo `01-javascript.js` con el contenido "Hola desde JavaScript".

8. **Configuración de URLs:**
   - En el archivo `urls.py` dentro de la aplicación `webapp`:
     ```python
     from django.urls import path
     from .views import javascript_request

     urlpatterns = [
         path('javascript_request/', javascript_request, name='javascript_request'),
     ]
     ```
   - Registrar las URLs de la aplicación en el archivo `urls.py` del proyecto.

9. **Creación de una Plantilla HTML (`javascript_request.html`):**
   ```html
   <!DOCTYPE html>
   <html lang="es">
   <head>
       <meta charset="utf-8">
       <meta name="viewport" content="width=device-width, initial-scale=1">
       <title>Hello, World!</title>
   </head>
   <body>
       <h1>Hello, World!</h1>
       <script type="text/javascript" src="{% static 'webapp/js/01-javascript.js' %}"></script>
   </body>
   </html>
   ```

10. **Ejecución del Servidor de Desarrollo:**
    ```bash
    python manage.py runserver
    ```

