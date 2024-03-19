# Tema 3: Estructuras de Datos

## 1. Scripts

### Definición y Utilidad
Un script es un conjunto de instrucciones o comandos que se ejecutan de manera secuencial para llevar a cabo una tarea específica. Estos son utilizados en programación para automatizar acciones y simplificar procesos repetitivos.

#### Ejemplo:
```python
# Ejemplo de un script en Python para imprimir un saludo
print("Hola, mundo!")
```

## 2. Estructura

### Concepto y Variedades
En programación, una estructura es una forma de organizar y almacenar datos relacionados. Puede ser tan simple como una variable o más compleja, como una lista o un diccionario, proporcionando flexibilidad en la gestión de la información.

#### Ejemplo:
```python
# Ejemplo de una estructura de lista en Python
mi_lista = [1, 2, 3, 4, 5]
```

## 3. Concatenar

### Acción y Aplicación
Concatenar implica unir dos o más cadenas de caracteres o elementos en una sola secuencia. Esta acción es comúnmente utilizada en la manipulación de cadenas de texto.

#### Ejemplo:
```python
# Ejemplo de concatenación de cadenas en Python
nombre = "Juan"
apellido = "Pérez"
nombre_completo = nombre + " " + apellido
print(nombre_completo)
```

## 4. Valor de Asignación

### Proceso y Operador
El valor de asignación es el acto de dar un valor a una variable o estructura de datos mediante el uso del operador de asignación (=) en la mayoría de los lenguajes de programación.

#### Ejemplo:
```python
# Ejemplo de valor de asignación en Python
edad = 25
```

## 5. Condiciones

### Evaluación y Decisiones
Las condiciones son expresiones que evalúan si una afirmación es verdadera o falsa. Las estructuras de control de flujo, como las sentencias "if" y "else," se utilizan para tomar decisiones basadas en estas condiciones.

#### Ejemplo:
```python
# Ejemplo de condición en Python
edad = 18
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

## 6. Palabras Reservadas

### Definición y Limitaciones
Las palabras reservadas son términos específicos que el lenguaje de programación reserva para su propio uso y no pueden ser utilizados como nombres de variables o funciones. Ejemplos incluyen "if," "else," "while" y "for."

#### Ejemplo:
```python
# Uso de palabra reservada "if" en Python
if condicion:
    # Código
```

## 7. Herencia

### Concepto y Aplicación
La herencia es un concepto en programación orientada a objetos que permite que una clase herede atributos y métodos de otra clase. Esto fomenta la reutilización de código y la creación de jerarquías de clases.

#### Ejemplo:
```python
# Ejemplo de herencia en Python
class Animal:
    def comer(self):
        print("El animal está comiendo.")

class Perro(Animal):
    def ladrar(self):
        print("¡Guau!")

mi_perro = Perro()
mi_perro.comer()
mi_perro.ladrar()
```

## 8. Agregación

### Composición y Construcción
La agregación se refiere a la composición de objetos o estructuras de datos complejas a partir de objetos más simples. Esto se logra combinando objetos en una relación "todo-parte."

#### Ejemplo:
```python
# Ejemplo de agregación en Python
class Rueda:
    def girar(self):
        print("La rueda está girando.")

class Auto:
    def __init__(self):
        self.rueda1 = Rueda()
        self.rueda2 = Rueda()

mi_auto = Auto()
mi_auto.rueda1.girar()
mi_auto.rueda2.girar()
```

## 9. Arreglo

### Definición y Propósito
Un arreglo es una estructura de datos que almacena una colección de elementos, generalmente del mismo tipo, en una secuencia ordenada. Se utilizan para almacenar datos de manera eficiente y acceder a ellos por índice.

#### Ejemplo:
```python
# Ejemplo de arreglo en Python
mi_arreglo = [1, 2, 3, 4, 5]
```

## 10. Lista (Arreglo Múltiple)

### Características y Adaptabilidad
Una lista es una estructura de datos que almacena una colección ordenada de elementos. En algunos lenguajes, se les conoce como "arreglos dinámicos" ya que pueden crecer o reducirse en tamaño dinámicamente.

#### Ejemplo:
```python
# Ejemplo de lista en Python
mi_lista = [1, 2, 3]
mi_lista.append(4)  # Añadir un elemento a la lista
```

## 11. Tupla

### Propiedades y Inmutabilidad
Una tupla es una estructura de datos similar a una lista pero a menudo inmutable, lo que significa que sus elementos no pueden modificarse una vez creados. Se utilizan para representar datos que no deben cambiar.

#### Ejemplo:
```python
# Ejemplo de tupla en Python
mi_tupla = (1, 2, 3)
```

## 12. Diccionario

### Características y Acceso Eficiente
Un diccionario es una estructura de datos que almacena datos en pares clave-valor. Permite acceder a los valores mediante sus claves, facilitando la búsqueda eficiente de información.

#### Ejemplo:
```python
# Ejemplo de diccionario en Python
mi_diccionario = {"clave1": "valor1", "clave2": "valor2"}
```

## 13. Arreglo Desordenado

### Utilidad y Enfoque
Un arreglo desordenado (o conjunto) es una estructura de datos que almacena elementos sin un orden específico. Se utiliza cuando solo se necesita verificar la presencia o ausencia de elementos en lugar de acceder a ellos por posición.

#### Ejemplo:
```python
# Ejemplo de conjunto en Python
mi_conjunto = {1, 2, 3, 4, 5}
``` 
