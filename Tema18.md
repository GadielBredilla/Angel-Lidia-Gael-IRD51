# Tema 18: Seguridad en Proyectos Django

1. **Manejo de Contraseñas:**
   - Configuración del manejo de contraseñas en Django.
   - Uso de la función `check_password()`.
     ```python
     # settings.py
     PASSWORD_HASHERS = [
         'django.contrib.auth.hashers.BCryptSHA256PasswordHasher',
     ]
     ```
     ```python
     # views.py
     from django.contrib.auth.hashers import check_password

     def verificar_contraseña(contraseña_ingresada, contraseña_hash):
         if check_password(contraseña_ingresada, contraseña_hash):
             print("La contraseña es correcta.")
         else:
             print("La contraseña es incorrecta.")
     ```

2. **Protección contra Ataques CSRF:**
   - Uso de `{% csrf_token %}` en formularios.
   - Configuración de middleware para protección contra CSRF.
     ```html
     <!-- formulario.html -->
     <form method="post">
         {% csrf_token %}
         <!-- resto del formulario -->
     </form>
     ```
     ```python
     # settings.py
     MIDDLEWARE = [
         # ...
         'django.middleware.csrf.CsrfViewMiddleware',
         # ...
     ]
     ```

3. **Protección contra Inyección de SQL:**
   - Uso de QuerySets y evitación de consultas SQL directas.
   - Configuración para evitar inyección de SQL.
     ```python
     # views.py
     from django.db import connection

     def consulta_personalizada(parametro):
         with connection.cursor() as cursor:
             cursor.execute("SELECT * FROM tabla WHERE columna = %s", [parametro])
             resultados = cursor.fetchall()
     ```

4. **Autenticación y Autorización:**
   - Uso de decoradores `login_required` y `permission_required`.
   - Personalización de backend de autenticación.
     ```python
     # views.py
     from django.contrib.auth.decorators import login_required, permission_required

     @login_required
     def vista_restringida(request):
         # contenido de la vista
     ```
     ```python
     # settings.py
     AUTHENTICATION_BACKENDS = ['miapp.backends.MiBackendDeAutenticacion']
     ```

5. **HTTPS y Configuración Segura:**
   - Configuración de Django para funcionar en modo seguro (HTTPS).
   - Configuración segura de la aplicación.
     ```python
     # settings.py
     SECURE_SSL_REDIRECT = True
     SESSION_COOKIE_SECURE = True
     CSRF_COOKIE_SECURE = True
     ```

6. **Control de Acceso a Vistas:**
   - Limitación del acceso a vistas según roles o permisos.
     ```python
     # views.py
     from django.contrib.auth.decorators import user_passes_test

     def es_administrador(user):
         return user.is_staff

     @user_passes_test(es_administrador)
     def vista_administrador(request):
         # contenido de la vista
     ```

