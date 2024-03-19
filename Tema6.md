# Tema 6: Programación Básica en Python con Ejemplos

## 1. Declarar Variables

En Python, las variables se declaran y asignan valores de manera dinámica:

```python
a = 12
print(a)
```

## 2. Ubicación de Variable

La ubicación de una variable puede ser local o global:

```python
def ejemplo_funcion():
    local_variable = 10
    print(local_variable)

ejemplo_funcion()
```

## 3. Declarar Arreglo

En Python, los arreglos se declaran utilizando listas:

```python
mi_lista = [1, 2, 3, 4]
print(mi_lista)
```

## 4. Print

La función `print()` se utiliza para mostrar información en la consola:

```python
mensaje = "Hola, Python!"
print(mensaje)
```

## 5. Concatenar

La concatenación combina cadenas de texto o variables:

```python
nombre = "Juan"
apellido = "Pérez"
nombre_completo = nombre + " " + apellido
print(nombre_completo)
```

## 6. Conversión

La conversión de tipos cambia el tipo de una variable:

```python
numero_entero = 5
numero_flotante = float(numero_entero)
print(numero_flotante)
```

## 7. Input

La función `input()` recibe datos del usuario:

```python
entrada_usuario = input("Ingrese su nombre: ")
print("Hola, " + entrada_usuario + "!")
```

## 8. Operadores Aritméticos

Python admite operadores aritméticos estándar:

```python
a = 5
b = 2
suma = a + b
resta = a - b
multiplicacion = a * b
division = a / b
print(suma, resta, multiplicacion, division)
```

## 9. Operadores de Asignación

Operadores como `+=` modifican el valor de una variable:

```python
x = 5
x += 3
print(x)  # Salida: 8
```

## 10. Operadores de Comparación

Operadores como `==`, `!=`, `<`, `>` comparan valores:

```python
a = 5
b = 7
print(a == b)  # Falso
```

## 11. Sentencias de Control

Las sentencias `if`, `else`, y `elif` toman decisiones:

```python
edad = 18
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

## 12. Tabulación

La tabulación define bloques de código:

```python
if condicion:
    print("Verdadero")
else:
    print("Falso")
```

## 13. Sentencia While

La sentencia `while` crea bucles:

```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

## 14. For

La sentencia `for` itera sobre secuencias:

```python
for i in range(5):
    print(i)
```

## 15. Diccionario en Python

Un diccionario almacena pares clave-valor:

```python
mi_diccionario = {'nombre': 'Ana', 'edad': 25}
print(mi_diccionario['nombre'])
```

## 16. Retornar Valores

Las funciones en Python pueden devolver valores:

```python
def suma(a, b):
    return a + b

resultado = suma(3, 4)
print(resultado)
```

## 17. Argumentos

Los argumentos se pasan a una función:

```python
def saludar(nombre, saludo="Hola"):
    print(saludo + ", " + nombre)

saludar("Carlos")
```

## 18. Listas

Las listas almacenan múltiples valores:

```python
numeros = [1, 2, 3, 4, 5]
print(numeros[2])  # Salida: 3
```

## 19. Llaves

Las llaves (`{}`) definen diccionarios y conjuntos:

```python
mi_diccionario = {'clave': 'valor'}
mi_conjunto = {1, 2, 3, 4}
```

## 20. Funciones

Las funciones permiten encapsular y reutilizar código:

```python
def saludar(nombre):
    print("Hola, " + nombre)

saludar("María")
```
