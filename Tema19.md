# Tema 19: Despliegue de Proyectos Django

1. **Configuración del Entorno de Producción:**
   - Ajustes de configuración para entornos de producción.
   - Uso de variables de entorno.
     ```python
     # settings.py
     import os
     DEBUG = os.getenv('DJANGO_DEBUG', 'False') == 'True'
     ```

2. **Servidores Web y WSGI:**
   - Configuración de servidores web como Nginx o Apache.
   - Uso de WSGI (gunicorn, uWSGI) con Django.
     ```bash
     gunicorn mysite.wsgi:application
     ```
     ```nginx
     # Configuración de Nginx
     server {
         listen 80;
         server_name dominio.com www.dominio.com;

         location = /favicon.ico { access_log off; log_not_found off; }
         location /static/ {
             root /ruta/a/tus/archivos;
         }

         location / {
             include proxy_params;
             proxy_pass http://127.0.0.1:8000;
         }
     }
     ```

3. **Despliegue en Plataformas de Nube:**
   - Des

pliegue en servicios en la nube como Heroku, AWS, o Google Cloud.
   - Configuración de bases de datos y almacenamiento en la nube.
     ```bash
     # Ejemplo de implementación en Heroku
     heroku create miapp
     git push heroku master
     heroku run python manage.py migrate
     ```

4. **Gestión de Versiones y Despliegue Continuo:**
   - Uso de herramientas como Git para gestión de versiones.
   - Implementación de despliegue continuo (CI/CD) con servicios como GitHub Actions.
     ```yaml
     # Configuración de GitHub Actions
     name: Despliegue Continuo

     on:
       push:
         branches:
           - main

     jobs:
       despliegue:
         runs-on: ubuntu-latest

         steps:
         - name: Checkout del código
           uses: actions/checkout@v2

         - name: Configurar entorno Python
           uses: actions/setup-python@v2
           with:
             python-version: 3.x

         - name: Instalar dependencias
           run: |
             python -m venv venv
             source venv/bin/activate
             pip install -r requirements.txt

         - name: Desplegar en servidor
           run: |
             python manage.py migrate
             # Otros comandos necesarios para el despliegue
     ```

5. **Manejo de Variables de Entorno en Producción:**
   - Configuración y uso de variables de entorno para secretos y configuraciones sensibles.
     ```python
     # settings.py
     import os
     SECRET_KEY = os.environ.get('DJANGO_SECRET_KEY')
     DEBUG = os.environ.get('DJANGO_DEBUG', 'False') == 'True'
     ```

