# Tema 7: JSON y Desarrollo Web

## 1. JSON (JavaScript Object Notation)

### Definición y Sintaxis
JSON es un formato ligero y legible por humanos para intercambiar datos entre aplicaciones. Utiliza una sintaxis similar a la de los objetos en JavaScript y consiste en pares clave-valor.

Ejemplo de JSON:

```json
{
  "nombre": "Juan",
  "edad": 25,
  "ciudad": "Ejemploville"
}
```

## 2. Clave Valor y Variable

En JSON, los datos se organizan en pares clave-valor. La clave es un identificador y el valor es el dato asociado. Esto facilita la organización de datos de manera estructurada.

Ejemplo de Clave Valor en JSON:

```json
{
  "producto": "Laptop",
  "precio": 1200,
  "disponible": true
}
```

## 3. Objeto, Propiedad y Atributos

Un objeto JSON es una colección no ordenada de pares clave-valor. Cada par clave-valor se denomina propiedad. Los valores pueden ser objetos, arreglos, cadenas, números, booleanos o null.

Ejemplo de Objeto JSON:

```json
{
  "estudiante": {
    "nombre": "María",
    "edad": 22,
    "cursos": ["Matemáticas", "Historia"]
  }
}
```

## 4. Laravel (Framework PHP)

### Características y Uso
Laravel es un framework de desarrollo web PHP conocido por su facilidad de uso, sintaxis elegante y características avanzadas. Ofrece herramientas para la gestión de bases de datos, autenticación de usuarios y creación de APIs.

Ejemplo de Uso en Laravel:

```php
// Ruta básica en Laravel
Route::get('/saludo', function () {
    return '¡Hola, Laravel!';
});
```

## 5. APIs (Interfaces de Programación de Aplicaciones)

### Definición y Utilidad
Las APIs son conjuntos de reglas y protocolos que permiten la comunicación entre aplicaciones. En desarrollo web, las APIs facilitan el acceso y la compartición de datos y funcionalidades entre aplicaciones web y servicios externos.

Ejemplo de Uso de una API en Python:

```python
import requests

response = requests.get("https://api.example.com/data")
data = response.json()
print(data)
```

## 6. pip (Administrador de Paquetes en Python)

### Función y Utilización
pip es una herramienta esencial en Python para instalar y gestionar paquetes. Facilita la incorporación de bibliotecas y módulos de terceros, contribuyendo al desarrollo eficiente de aplicaciones Python.

Ejemplo de Uso de pip:

```bash
pip install nombre_del_paquete
```

Estos conceptos son fundamentales en el desarrollo web moderno, donde la manipulación y transmisión eficiente de datos son cruciales para la interconexión de aplicaciones y servicios.

