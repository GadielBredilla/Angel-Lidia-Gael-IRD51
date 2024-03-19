# Tema 16: Introducción a API con Postman y Procesamiento de JSON en Python

En este tema, se explorará el uso de Postman para realizar solicitudes a una API (por ejemplo, la API de Pokémon). Además, se mostrará cómo procesar la respuesta JSON en Python utilizando la biblioteca `json` y la función `json.loads()`. A continuación, se detallan los pasos y ejemplos:

1. **Solicitud a una API con Postman:**
   - Abrir Postman e ingresar la URL de la API: `https://pokeapi.co/api/v2/pokemon/ditto`.
   - Enviar la solicitud y revisar la respuesta JSON.

2. **Procesamiento de JSON en Python:**
   - Importar la biblioteca `json` en el script de Python:
     ```python
     import json
     ```

3. **Convertir JSON a Cadena en Python:**
   - Obtener la respuesta JSON de la API (por ejemplo, almacenarla en la variable `json_response`).
   - Utilizar `json.dumps()` para convertir el JSON a una cadena:
     ```python
     json_string = json.dumps(json_response)
     ```

4. **Convertir Cadena a JSON en Python:**
   - Obtener una cadena JSON (por ejemplo, almacenarla en la variable `json_string`).
   - Utilizar `json.loads()` para convertir la cadena a JSON:
     ```python
     json_data = json.loads(json_string)
     ```

5. **Ejemplo Completo en Python:**
   ```python
   import json
   import requests

   # Realizar solicitud a la API
   response = requests.get('https://pokeapi.co/api/v2/pokemon/ditto')

   # Verificar si la solicitud fue exitosa (código de estado 200)
   if response.status_code == 200:
       # Obtener la respuesta JSON
       json_response = response.json()

       # Convertir JSON a cadena
       json_string = json.dumps(json_response, indent=2)
       print(f'JSON como cadena:\n{json_string}')

       # Convertir cadena a JSON
       json_data = json.loads(json_string)
       print(f'\nDatos JSON:\n{json_data}')
   else:
       print(f'Error en la solicitud: {response.status_code}')
   ```

6. **Notas Adicionales:**
   - Es fundamental manejar errores en las solicitudes a la API y el procesamiento de JSON para garantizar un flujo de ejecución sin problemas.
   - Postman es una herramienta poderosa para explorar y probar APIs, permitiendo ajustar parámetros y analizar respuestas de manera visual.

