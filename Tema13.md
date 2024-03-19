# Tema 13: Integración de JavaScript y Llamadas a API en Proyectos Django

1. **Modificar la plantilla `javascript.html` para incluir un botón que activará la llamada a la API:**

```html
{% load static %}

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="author" content="Angel Xdn">
    <title>Llamada a API desde Django</title>
</head>
<body>

    <h1>Llamada a API desde Django</h1>
    
    <!-- Botón para activar la llamada a la API -->
    <button onclick="llamarAPI()">Realizar Llamada a la API</button>

    <!-- Script de JavaScript para la llamada a la API -->
    <script src="{% static 'js/llamada_api.js' %}"></script>

</body>
</html>
```

2. **Crear el archivo `llamada_api.js` en la carpeta `webapp/static/js/` con el siguiente contenido:**

```javascript
function llamarAPI() {
    // URL de la API a la que llamaremos (reemplazar con la URL real)
    const urlAPI = "https://api.ejemplo.com/datos";

    // Realizar la llamada a la API usando el método fetch
    fetch(urlAPI)
        .then(response => response.json())
        .then(data => {
            // Procesar los datos recibidos de la API
            console.log("Datos recibidos de la API:", data);

            // Ejemplo de cómo mostrar datos en la página
            const resultado = document.createElement("p");
            resultado.innerHTML = `Datos de la API: ${JSON.stringify(data)}`;
            document.body.appendChild(resultado);
        })
        .catch(error => {
            // Manejar errores en la llamada a la API
            console.error("Error en la llamada a la API:", error);
        });
}
```

3. **Asegúrate de que tu configuración `settings.py` contenga la configuración para archivos estáticos:**

```python
# settings.py

# ...

STATIC_URL = '/static/'

# Ruta donde se almacenarán los archivos estáticos (js, css, etc.)
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'webapp/static/'),
]

# ...
```

4. **Asegúrate de que la carpeta `webapp/static/js/` contenga el archivo `llamada_api.js`.**

5. **Asegúrate de que la URL en `const urlAPI` sea la correcta y corresponda a la API que deseas llamar.**

6. **Cuando se hace clic en el botón "Realizar Llamada a la API" en la página, se activará la función `llamarAPI()`, que realizará la llamada a la API y mostrará los datos recibidos en la consola y en la página.**


