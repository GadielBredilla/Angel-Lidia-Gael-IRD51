# Tema 14: Estructuras de Control en JavaScript y Trabajo con Datos

En este tema, exploraremos diferentes estructuras de control en JavaScript y cómo trabajar con datos utilizando arreglos, funciones y objetos. Se abordarán conceptos clave como bucles (`while`), arreglos, funciones de distintos tipos, y cómo manejar diccionarios JSON y realizar llamadas a una API. A continuación, se presentan los puntos clave con ejemplos de código:

1. **Bucle While en JavaScript:**
   ```javascript
   let numero = 1;
   const limite = 10;

   while (numero <= limite) {
       const resultado = numero / 2;
       if (numero % 2 === 0) {
           console.log(`${numero} dividido entre 2 es igual a ${resultado}`);
       }
       numero += 1;
   }
   ```

2. **Trabajo con Arreglos en JavaScript:**
   ```javascript
   const nombres = ["Monse", "Liz", "Daniel", "Anel"];
   const longitud = nombres.length;

   console.log(`Longitud del arreglo: ${longitud}`);
   console.log("Nombres en el arreglo:");
   for (let i = 0; i < longitud; i++) {
       console.log(nombres[i]);
   }
   ```

3. **Funciones en JavaScript:**
   - Función tipo `void` (sin retorno):
     ```javascript
     function sumar(a, b) {
         console.log(a + b);
     }

     sumar(10, 20);
     ```

   - Función tipo `return` (con retorno):
     ```javascript
     function restar(a, b) {
         return a - b;
     }

     console.log(restar(10, 2));
     ```

   - Función tipo flecha:
     ```javascript
     const recorrer = (arreglo) => {
         if (Array.isArray(arreglo)) {
             for (let i = 0; i < arreglo.length; i++) {
                 console.log(arreglo[i]);
             }
         }
     };

     // Ejemplo de uso de la función
     const miArreglo = [1, 2, 3, 4, 5];
     recorrer(miArreglo);
     ```

4. **Diccionario JSON en JavaScript:**
   ```json
   {
     "empleados": [
       {"nombre": "Ariel", "apellido": "Lozano"},
       {"nombre": "Gabriel", "apellido": "Fuentes"},
       {"nombre": "Ana", "apellido": "Flores"}
     ]
   }
   ```

   ```javascript
   const json = '{"empleados": [{"nombre": "Ariel","apellido": "Lozano"}, {"nombre": "Gabriel","apellido": "Fuentes"}, {"nombre": "Ana","apellido": "Flores"}]}';

   const data = JSON.parse(json);
   const [empleado1, empleado2, empleado3] = data.empleados;
   const { nombre, apellido } = empleado1;
   console.log(nombre, apellido);
   ```

5. **Llamadas a una API en JavaScript:**
   ```javascript
   const dataUser = (json) => {
       const data = JSON.parse(JSON.stringify(json));
       const [user1, ...rest] = data;
       console.log(user1, '\n');
       console.log(user1.id, user1.name, user1.username);
       console.log(user1.address.street, user1.address.city);
   };

   fetch('http://xdn.com/json.php')
       .then((response) => response.json())
       .then((json) => dataUser(json));
   ```

