# Tema 4: Sentencias de Control y Operadores de Comparación

## Sentencias de Control

### if-elif-else

La sentencia `if` se utiliza para tomar decisiones en el código, ejecutando un bloque de código si una condición es verdadera. Se puede combinar con `elif` y `else` para manejar múltiples condiciones.

```python
if condicion:
    # Código a ejecutar si la condición es verdadera
elif otra_condicion:
    # Código a ejecutar si otra_condición es verdadera
else:
    # Código a ejecutar si ninguna de las condiciones anteriores es verdadera
```

#### Ejemplo:
```python
edad = 18
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

### for

La sentencia `for` se utiliza para iterar sobre una secuencia (como una lista, tupla o cadena) o cualquier objeto iterable. Permite ejecutar un bloque de código para cada elemento de la secuencia.

```python
for elemento in secuencia:
    # Código a ejecutar para cada elemento
```

#### Ejemplo:
```python
numeros = [1, 2, 3, 4, 5]
for num in numeros:
    print(num)
```

### while

La sentencia `while` se utiliza para crear bucles que se ejecutan mientras una condición sea verdadera. El bloque de código se repetirá hasta que la condición sea falsa.

```python
while condicion:
    # Código a ejecutar mientras la condición sea verdadera
```

#### Ejemplo:
```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

### break

La palabra clave `break` se utiliza para salir de un bucle (for o while) antes de que se complete su ejecución normal.

```python
for elemento in secuencia:
    if condicion:
        break
```

### continue

La palabra clave `continue` se utiliza para saltar la iteración actual en un bucle y continuar con la siguiente iteración.

```python
for elemento in secuencia:
    if condicion:
        continue
```

### pass

La sentencia `pass` no hace nada y se utiliza como marcador de posición cuando se requiere una sentencia en una estructura de control pero no se necesita ninguna acción.

```python
if condicion:
    pass
```

## Operadores de Comparación

### Igualdad (==)

Comprueba si dos valores son iguales.

```python
a == b  # Verdadero si a es igual a b
```

### Desigualdad (!=)

Comprueba si dos valores son diferentes.

```python
a != b  # Verdadero si a no es igual a b
```

### Mayor que (>)

Comprueba si un valor es mayor que otro.

```python
a > b  # Verdadero si a es mayor que b
```

### Menor que (<)

Comprueba si un valor es menor que otro.

```python
a < b  # Verdadero si a es menor que b
```

### Mayor o igual que (>=)

Comprueba si un valor es mayor o igual que otro.

```python
a >= b  # Verdadero si a es mayor o igual que b
```

### Menor o igual que (<=)

Comprueba si un valor es menor o igual que otro.

```python
a <= b  # Verdadero si a es menor o igual que b
```

Estos operadores son fundamentales para realizar comparaciones y tomar decisiones en las sentencias de control, proporcionando la lógica necesaria para dirigir el flujo de ejecución del programa.

