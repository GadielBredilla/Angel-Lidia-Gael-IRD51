# Tema 9: Django y sus Aplicativos

## Django y su Objetivo

Django es un framework de desarrollo web de código abierto escrito en Python. Su objetivo principal es simplificar la creación de aplicaciones web, proporcionando herramientas y patrones para el desarrollo eficiente y estructurado.

## Características de Django

### 1. Arquitectura MVC (Model-View-Controller)

Django sigue el patrón de arquitectura MVC, que ayuda a separar claramente la lógica de la aplicación en tres componentes: el modelo (Model), la vista (View) y el controlador (Controller).

### 2. Administrador

Django proporciona un administrador automático que facilita la gestión de los datos del sitio web. Esto simplifica las tareas relacionadas con la administración de contenidos y la gestión de la base de datos.

### 3. ORM (Object-Relational Mapping)

Django utiliza un ORM que permite interactuar con la base de datos utilizando objetos de Python en lugar de trabajar directamente con SQL. Esto facilita la manipulación de datos y mejora la portabilidad entre diferentes sistemas de gestión de bases de datos.

### 4. Sistema de Enrutamiento

Django tiene un sistema de enrutamiento que asigna las URL a vistas de manera rápida y flexible, facilitando la creación y gestión de rutas.

### 5. Plantillas Reutilizables

Utiliza un sistema de plantillas único que permite definir la apariencia de las páginas web de manera lógica y separada del código Python, simplificando la creación de interfaces de usuario atractivas.

### 6. Autenticación y Autorización

Proporciona mecanismos autorizados y autenticados de usuarios, simplificando el sistema de registro y acceso seguro a las aplicaciones.

### 7. AdminSite

Permite a los desarrolladores personalizar y gestionar fácilmente modelos de datos en la interfaz de administración de Django, definiendo cómo se muestran, editan y gestionan los datos de la aplicación.

### 8. Seguridad

Django se enfoca en la seguridad, proporcionando protección contra vulnerabilidades comunes, como ataques de SQL y CSRF (Cross-Site Request Forgery).

### 9. Insensibilidad

Refiere la forma en que se manejan las consultas a la base de datos en cuanto a mayúsculas y minúsculas, lo que significa que distingue entre estos tipos de letras para la búsqueda de datos en la base de datos.

### 10. Escalabilidad

Diseñado para facilitar la escalabilidad de las aplicaciones web, permitiendo que un proyecto pueda crecer según las necesidades sin perder eficiencia.

## Django vs Laravel

Django y Laravel son dos frameworks populares, siendo Django específico de Python y Laravel de PHP. Ambos comparten características similares, pero la elección entre ellos generalmente depende del lenguaje de programación preferido y los requisitos del proyecto.

## Vista Controlador

Django sigue una arquitectura similar al patrón Modelo-Vista-Controlador (MVC). La vista controladora en Django se llama "view" y se encarga de procesar las solicitudes del usuario y devolver las respuestas apropiadas.

## Vista Emplea Modelo

En Django, las vistas emplean el modelo para interactuar con la base de datos y recuperar los datos necesarios para responder a las solicitudes del usuario.

## Ejemplos de Código

### 1. Modelo en Django:

```python
from django.db import models

class Producto(models.Model):
    nombre = models.CharField(max_length=100)
    descripcion = models.TextField()
    precio = models.DecimalField(max_digits=10, decimal_places=2)

    def __str__(self):
        return self.nombre
```

### 2. Vista en Django:

```python
from django.shortcuts import render
from .models import Producto

def lista_productos(request):
    productos = Producto.objects.all()
    return render(request, 'lista_productos.html', {'productos': productos})
```

### 3. Plantilla HTML (`lista_productos.html`):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lista de Productos</title>
</head>
<body>
    <h1>Lista de Productos</h1>
    <ul>
        {% for producto in productos %}
            <li>{{ producto.nombre }} - {{ producto.precio }}</li>
        {% endfor %}
    </ul>
</body>
</html>
```

### 4. Creación de una Aplicación en Django:

```bash
python manage.py startapp miapp
```

### 5. Modelo en una Aplicación Django (`miapp/models.py`):

```python
from django.db import models

class MiModelo(models.Model):
    nombre = models.CharField(max_length=

100)
    fecha_creacion = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.nombre
```

### 6. Registrar la Aplicación en la Configuración de Django (`settings.py`):

```python
INSTALLED_APPS = [
    # ...
    'miapp',
    # ...
]
```

### 7. URL para la Aplicación (`miapp/urls.py`):

```python
from django.urls import path
from . import views

urlpatterns = [
    path('objetos/', views.lista_objetos, name='lista_objetos'),
]
```

### 8. Registrar la URL de la Aplicación en el Proyecto (`urls.py`):

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('miapp/', include('miapp.urls')),
]
```

## Método del Código PAT (Patrón de Autenticación)

El método del Código PAT es una autenticación segura utilizado en aplicaciones web. Incluye los siguientes pasos:

1. **Crear un PAT:** Generar un Código de Acceso Personal (PAT).
2. **Almacenar:** Guardar el PAT de manera segura.
3. **Utilizar:** Utilizar el PAT para autenticar las solicitudes a la aplicación.
4. **Renovar y Revocar:** Renovar el PAT periódicamente y tener la capacidad de revocar el acceso si es necesario.

## Template

En Django, un template es un archivo que contiene código HTML con incorporación de etiquetas y variables de Python para generar dinámicamente el contenido de una página web.

Para acceder a los parámetros dentro de un template de Django, se utilizan las dobles llaves (`{{ variable }}`). Estas llaves indican a Django que debe reemplazarlas con el valor de la variable proporcionada.
