# Tema 11: Configuración Inicial y Desarrollo Básico con Django

En este tema, exploramos los pasos iniciales para configurar un proyecto Django, incluyendo la creación del proyecto, instalación de dependencias, configuración del entorno virtual y creación de una aplicación dentro del proyecto. Además, se abordan conceptos como la activación del entorno virtual, ejecución del servidor de desarrollo y la importación de funciones desde el módulo de vistas. Este conjunto de pasos sienta las bases para el desarrollo web con Django y proporciona una introducción al entorno de desarrollo y las herramientas esenciales.

### Creación de un Proyecto Django

```bash
django-admin startproject mysite
```

Este comando inicia un nuevo proyecto Django llamado "mysite". Un proyecto en Django es una colección de configuraciones y aplicaciones que trabajan juntas para cumplir con un objetivo específico.

### Instalación de la Biblioteca `psycopg2`

```bash
pip install psycopg2
```

`psycopg2` es un adaptador de base de datos PostgreSQL para Python. Este paso indica que estás instalando esta biblioteca para trabajar con una base de datos PostgreSQL en tu proyecto Django. Específicamente, se usa para conectar Django con la base de datos PostgreSQL.

### Creación de un Entorno Virtual

```bash
python -m venv .env
```

Un entorno virtual es un espacio aislado donde se pueden instalar dependencias de Python sin afectar el sistema global. Esto ayuda a evitar conflictos entre versiones de paquetes y facilita la gestión de las dependencias de tu proyecto.

### Iniciar el Entorno Virtual

```bash
source .env/bin/activate  # en sistemas basados en Unix/Linux
```

```bash
.env\Scripts\activate  # en sistemas basados en Windows
```

Activar el entorno virtual asegura que las dependencias instaladas y los comandos de Python están aislados dentro del entorno y no afectan el sistema global.

### Iniciar el Servidor de Desarrollo de Django

```bash
python manage.py runserver
```

Este comando inicia el servidor de desarrollo de Django, que te permite probar y desarrollar tu aplicación localmente. Puedes acceder a tu aplicación desde un navegador web visitando la dirección `http://localhost:8000`.

### Crear una Aplicación en el Proyecto

```bash
python manage.py startapp webapp
```

Este comando crea una nueva aplicación llamada "webapp" dentro del proyecto. Las aplicaciones en Django son módulos reutilizables que pueden contener modelos, vistas y plantillas. Cada aplicación tiene su propio propósito y funcionalidad dentro del proyecto.

### Importar Funciones desde `webapp.views`

```python
from webapp.views import ...  # Agrega tus importaciones específicas aquí
```

Esto sugiere que estás importando funciones o clases desde el módulo `views` dentro de la aplicación "webapp". Las vistas en Django manejan la lógica detrás de las páginas web y determinan qué se muestra al usuario.

### Configuración de la Base de Datos en `.env`

El archivo `.env` generalmente se utiliza para almacenar configuraciones sensibles, como claves secretas o credenciales de bases de datos. Si estás utilizando PostgreSQL, puedes configurar las credenciales de la base de datos en este archivo.

### Comando para Aplicar Migraciones

```bash
python manage.py migrate
```

Este comando aplica las migraciones pendientes en tu base de datos. Las migraciones en Django son un sistema para evolucionar tu esquema de base de datos a lo largo del tiempo.

Estos pasos forman parte de la configuración y creación inicial de un proyecto Django junto con la creación de una aplicación dentro del proyecto. Recuerda ajustar según las necesidades específicas de tu proyecto, como configuraciones de base de datos, modelos, vistas y URL.
