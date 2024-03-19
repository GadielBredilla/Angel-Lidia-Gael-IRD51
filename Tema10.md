# Tema 10: Desarrollo de Aplicación con Django

## Introducción

En este tema, exploraremos el desarrollo de una aplicación en Django, haciendo hincapié en la implementación de múltiples variables, el uso de plantillas basadas en Django, la creación de funciones dinámicas con Python y HTML, y la interacción con formularios.

## Librerías y Bibliotecas en Django

Django hace uso extenso de diversas bibliotecas y módulos para simplificar el desarrollo web. Algunas de las librerías fundamentales son:

- **django.http:** Proporciona clases para manejar respuestas HTTP y solicitudes.

- **datetime:** Módulo estándar de Python que maneja fechas y horas.

- **django.shortcuts:** Contiene funciones y clases de utilidad para el desarrollo rápido con Django.

## Ejemplo de una Aplicación Django

Consideremos un escenario simple donde creamos una aplicación que saluda al usuario, realiza operaciones matemáticas básicas y muestra el resultado.

### Estructura del Proyecto

- **Proyecto: myproject**
  - **Aplicación: myapp**

### Archivo `views.py` (Controlador y Vistas)

```python
from django.shortcuts import render
from django.http import HttpResponse
from datetime import datetime

def saludo(request):
    return HttpResponse("Hola, bienvenido a nuestra aplicación Django.")

def operaciones(request, operacion, num1, num2):
    if operacion == 'suma':
        resultado = num1 + num2
        signo = '+'
    elif operacion == 'resta':
        resultado = num1 - num2
        signo = '-'
    elif operacion == 'multiplicacion':
        resultado = num1 * num2
        signo = '*'
    elif operacion == 'division':
        if num2 != 0:
            resultado = num1 / num2
            signo = '/'
        else:
            return HttpResponse("Error: División por cero.")
    else:
        return HttpResponse("Operación no válida.")

    mensaje = f"El resultado de {num1} {signo} {num2} es: {resultado}"
    return render(request, 'operaciones.html', {'mensaje': mensaje})

def tiempo_actual(request):
    now = datetime.now()
    return render(request, 'tiempo_actual.html', {'hora_actual': now})
```

### Archivo `urls.py`

```python
from django.urls import path
from .views import saludo, operaciones, tiempo_actual

urlpatterns = [
    path('saludo/', saludo, name='saludo'),
    path('operaciones/<str:operacion>/<int:num1>/<int:num2>/', operaciones, name='operaciones'),
    path('tiempo_actual/', tiempo_actual, name='tiempo_actual'),
]
```

### Archivo `urls.py` del Proyecto

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('myapp/', include('myapp.urls')),
]
```

### Archivo `operaciones.html` (Plantilla)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Operaciones Matemáticas</title>
</head>
<body>
    <h1>{{ mensaje }}</h1>
</body>
</html>
```

### Archivo `tiempo_actual.html` (Plantilla)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tiempo Actual</title>
</head>
<body>
    <h1>La hora actual es: {{ hora_actual }}</h1>
</body>
</html>
```

## Explicación y Detalles

1. **Saludo:** La vista `saludo` simplemente devuelve un mensaje de bienvenida.

2. **Operaciones Matemáticas:** La vista `operaciones` realiza operaciones básicas (suma, resta, multiplicación, división) según la solicitud del usuario y muestra el resultado en la plantilla `operaciones.html`.

3. **Tiempo Actual:** La vista `tiempo_actual` utiliza el módulo `datetime` para obtener la hora actual y la muestra en la plantilla `tiempo_actual.html`.

4. **Estructura de URLs:** Las rutas definidas en `urls.py` determinan qué vista debe manejar una solicitud específica. Por ejemplo, la ruta `'operaciones/<str:operacion>/<int:num1>/<int:num2>/'` permite pasar parámetros a la vista `operaciones`.

5. **Plantillas Basadas en Django:** Las plantillas permiten incrustar código Python (dentro de las llaves dobles `{{ ... }}`) para generar contenido dinámico. En los ejemplos, `mensaje` y `hora_actual` son variables que se pasan desde las vistas a las plantillas.

6. **Mensajes de Error:** Se incluyen verificaciones para evitar divisiones por cero y para manejar operaciones no válidas.

