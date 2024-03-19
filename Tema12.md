# Tema 12: Integración de JavaScript en Proyectos Django

En este tema, exploraremos la integración de JavaScript en proyectos Django. Se abordarán conceptos clave de JavaScript, como la declaración de variables (`var`, `let`, `const`), funciones y el uso de objetos. Además, se destacará la relación entre Python (usado en Django) y JavaScript, y cómo estos lenguajes pueden interactuar para lograr una experiencia de desarrollo más completa.

## Contenido del Tema:

1. **Declaración de Variables en JavaScript:**
   - `var`, `let` y `const`: Diferencias y usos.
   - Ejemplos de declaración de variables.


```javascript
// Uso de var (funciona en todo el ámbito)
var x = 10;

// Uso de let (ámbito de bloque)
let y = 20;

// Uso de const (constante, no puede ser reasignada)
const PI = 3.14;
```

2. **Funciones en JavaScript:**
   - Declaración de funciones y uso de la palabra clave `function`.
   - Funciones de una sola línea y el uso de `return`.
   - Ejemplos prácticos.

```javascript
// Declaración de una función
function sumar(a, b) {
    return a + b;
}

// Función de una sola línea
let resta = (a, b) => a - b;

// Uso de funciones
console.log(sumar(5, 3));  // Resultado: 8
console.log(resta(10, 4));  // Resultado: 6
```

3. **Uso de Objetos en JavaScript:**
   - Creación y manipulación de objetos en JavaScript.
   - Acceso a propiedades de objetos mediante notación de punto y corchetes.
   - Ejemplos de objetos en el contexto de desarrollo web.

```javascript
// Creación de un objeto
let persona = {
    nombre: "Juan",
    edad: 30,
    ciudad: "Ejemploville"
};

// Acceso a propiedades
console.log(persona.nombre);  // Resultado: Juan
console.log(persona["edad"]);  // Resultado: 30
```

4. **Integración de JavaScript en Proyectos Django:**
   - Relación entre Django (Python) y JavaScript en el desarrollo web.
   - Uso de JavaScript para mejorar la interactividad en las aplicaciones web Django.
   - Ejemplos de integración de JavaScript en plantillas Django.

En un archivo de plantilla Django (`mi_template.html`):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Página con JavaScript</title>
</head>
<body>
    <h1>Bienvenido a mi página</h1>
    
    <!-- Uso de JavaScript en un bloque script -->
    <script>
        // Declaración y uso de variables
        var mensaje = "Hola desde JavaScript";
        console.log(mensaje);

        // Integración con variables de Django
        var nombreDjango = "{{ nombre_django }}";
        console.log("Nombre desde Django: " + nombreDjango);
    </script>
</body>
</html>
```

5. **APIs y Comunicación con el Servidor:**
   - Concepto de APIs y su papel en la comunicación entre el frontend y el backend.
   - Ejemplos de llamadas a API desde JavaScript en un entorno Django.

```javascript
// Ejemplo de llamada a una API desde JavaScript en Django
fetch('/api/datos/')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

6. **Variables, Constantes y Funciones en Django con JavaScript:**
   - Declaración de variables y constantes en Django templates con JavaScript.
   - Uso de funciones en el contexto de plantillas Django.
   - Ejemplos prácticos de la integración de JavaScript en aplicaciones Django.

En un archivo de plantilla Django (`integracion_django_js.html`):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Integración Django y JavaScript</title>
</head>
<body>
    <h1>Integración de Django y JavaScript</h1>
    
    <!-- Uso de variables y constantes de Django en JavaScript -->
    <script>
        var nombreDjango = "{{ nombre_django }}";
        const PI = {{ constante_pi }};
        
        console.log("Nombre desde Django: " + nombreDjango);
        console.log("Valor de PI desde Django: " + PI);
        
        // Uso de funciones de Django en JavaScript
        function saludarDjango() {
            alert("¡Hola, " + nombreDjango + "!");
        }
    </script>
</body>
</html>
```

7. **Transpilación y Migración de Código:**
   - Concepto de transpilación y su aplicación en proyectos Django con JavaScript.
   - Uso de herramientas como Babel para transpilar código JavaScript.
   - Migración de sectores de código entre diferentes lenguajes en proyectos Django.

Transpilación con Babel:

1. **Instalar Babel:**
   ```bash
   npm install @babel/core @babel/cli @babel/preset-env --save-dev
   ```

2. **Configuración de Babel (`babel.config.js`):**
   ```javascript
   module.exports = {
       presets: ['@babel/preset-env']
   };
   ```

3. **Transpilar con Babel:**
   ```bash
   npx babel archivo.js -o archivo-transpilado.js
   ```


8. **Manejo de Variables Tipo String:**
   - Exploración de variables tipo string en JavaScript.
   - Restricciones y ejemplos de uso.
   - Comparación con variables en otros lenguajes como Python.

```javascript
// Variables tipo string en JavaScript
let nombre = "Juan";
let saludo = `Hola, ${nombre}!`;

console.log(saludo);  // Resultado: Hola, Juan!
```

9. **Integración de JavaScript con Django:**
   - Uso de JavaScript en conjunto con plantillas Django.
   - Ejemplos de integración de funciones y variables entre Django y JavaScript.

En un archivo de plantilla Django (`integracion_django_js.html`):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Integración Django y JavaScript (Continuación)</title>
</head>
<body>
    <h1>Integración de Django y JavaScript (Continuación)</h1>
    
    <!-- Uso de variables y constantes de Django en JavaScript -->
    <script>
        var nombreDjango = "{{ nombre_django }}";
        const PI = {{ constante_pi }};
        
        console.log("Nombre desde Django: " + nombreDjango);
        console.log("Valor de PI desde Django: " + PI);
        
        // Uso de funciones de Django en JavaScript
        function saludarDjango() {
            alert("¡Hola, " + nombreDjango + "!");
        }
        
        // Integración con elementos HTML
        document.getElementById("mensaje-django").innerHTML = "Mensaje desde Django: " + nombreDjango;
    </script>

    <!-- Elemento HTML para integración -->
    <p id="mensaje-django"></p>
</body>
</html>
```

10. **Consideraciones sobre Variables Inmutables en JavaScript:**
    - Entendimiento de variables inmutables y su relación con `const` en JavaScript.
    - Ejemplos de variables inmutables y su uso en proyectos Django.

```javascript
// Variables inmutables en JavaScript con const
const numero = 42;

// Esto dará un error
// numero = 50;
```

11. **Migración y Transpilación de Código:**
    - Uso de herramientas de transpilación para migrar código entre diferentes lenguajes.
    - Ejemplos de migración de código entre Python y JavaScript en proyectos Django.

Ejemplo de migración de código entre Python y JavaScript:

```python
# Código en Python
def saludar_python(nombre):
    return f"Hola, {nombre} desde Python!"

# Transpilación a JavaScript usando Babel
# function saludar_python(nombre) {
#     return `Hola, ${nombre} desde Python!`;
# }
```

12. **Declaración de Variables en Python y JavaScript:**
    - Comparación de la declaración de variables en Python y JavaScript.
    - Ejemplos de similitudes y diferencias en la sintaxis.

```python
# Declaración de variables en Python
nombre_python = "Juan"
edad_python = 25

# Declaración de variables en JavaScript (ejemplo continuación)
<script>
    var nombreJS = "{{ nombre_js }}";
    var edadJS = {{ edad_js }};
</script>
```

