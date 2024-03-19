# Tema 2: Lenguajes de Programación

## 1. Lenguaje de Programación

### Definición y Clasificación
Un lenguaje de programación se define como un conjunto de reglas, instrucciones y convenciones que permiten a los programadores comunicarse con una computadora para desarrollar software y aplicaciones. Estos lenguajes pueden clasificarse según su nivel de abstracción. Por ejemplo, existen lenguajes de alto nivel como Python, Java y C++, que proporcionan abstracciones más cercanas al lenguaje humano. Por otro lado, lenguajes de bajo nivel como C o Assembly ofrecen un mayor control sobre los recursos de hardware, pero a costa de una mayor complejidad.

#### Ejemplo:
```python
# Ejemplo de código en Python
def saludar(nombre):
    print("Hola, " + nombre)

saludar("Juan")
```

## 2. Código Abierto

### Concepto y Filosofía
El código abierto implica la disponibilidad pública del código fuente de un software, permitiendo su acceso, modificación y distribución libre. Proyectos como Linux y Mozilla Firefox son ejemplos notables. Este enfoque promueve la colaboración y transparencia, permitiendo que la comunidad contribuya y mejore el software de manera colectiva.

#### Ejemplo:
- El sistema operativo Linux, donde el código fuente está disponible para que cualquier persona lo explore, modifique y distribuya según sus necesidades.

## 3. Bibliotecas

### Función y Utilidad
Las bibliotecas son conjuntos de funciones predefinidas que facilitan a los programadores realizar tareas comunes sin tener que escribir todo el código desde cero. Pueden ser parte del lenguaje estándar o desarrolladas por terceros. En Python, la biblioteca estándar incluye módulos para diversas tareas como manejo de archivos, manipulación de cadenas y acceso a Internet.

#### Ejemplo:
```python
# Uso de la biblioteca estándar de Python para manejo de archivos
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
```

## 4. Supertabilidad (Supertyping)

### Concepto y Flexibilidad
La supertabilidad se refiere a la capacidad de un lenguaje de programación para manejar tipos de datos de manera más general o genérica. Lenguajes que admiten supertipos permiten que variables contengan datos de diferentes tipos, brindando flexibilidad en el desarrollo y reutilización de código. Python es un ejemplo, siendo un lenguaje fuertemente tipado pero dinámico, lo que permite que las variables cambien de tipo durante la ejecución.

#### Ejemplo:
```python
# Ejemplo de supertabilidad en Python
x = 5        # x es de tipo entero
x = "Hola"   # x ahora es una cadena de texto
```

