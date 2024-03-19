# Tema 18: Trabajo con Bases de Datos en Proyectos Django

1. **Configuración de Base de Datos en Django:**
   - Configuración para bases de datos SQLite, PostgreSQL, MySQL, etc.
     ```python
     # settings.py
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.sqlite3',
             'NAME': BASE_DIR / "db.sqlite3",
         }
     }
     ```

2. **Modelos en Django:**
   - Creación de modelos en Django.
   - Definición de campos y relaciones.
     ```python
     # models.py
     from django.db import models

     class Persona(models.Model):
         nombre = models.CharField(max_length=100)
         edad = models.IntegerField()
         ```

3. **Migraciones en Django:**
   - Generación y aplicación de migraciones.
     ```bash
     python manage.py makemigrations
     python manage.py migrate
     ```

4. **Consultas y Filtros:**
   - Uso de QuerySets para realizar consultas.
   - Filtrado de datos con el método `filter()`.
     ```python
     # views.py
     def personas_mayores(request):
         personas_mayores = Persona.objects.filter(edad__gte=18)
         ```

5. **Relaciones entre Modelos:**
   - Relaciones de uno a uno, uno a muchos y muchos a muchos.
     ```python
     # models.py
     class Ciudad(models.Model):
         nombre = models.CharField(max_length=100)

     class Persona(models.Model):
         nombre = models.CharField(max_length=100)
         ciudad = models.ForeignKey(Ciudad, on_delete=models.CASCADE)
     ```

6. **Vistas Basadas en Modelos:**
   - Uso de vistas basadas en modelos para mostrar y manejar datos de la base de datos.
     ```python
     # views.py
     from django.views.generic import ListView
     from .models import Persona

     class ListaPersonas(ListView):
         model = Persona
         template_name = 'lista_personas.html'
     ```

7. **Formularios y ModelForms:**
   - Creación de formularios para interactuar con modelos.
   - Uso de ModelForms para simplificar la creación de formularios basados en modelos.
     ```python
     # forms.py
     from django import forms
     from .models import Persona

     class PersonaForm(forms.ModelForm):
         class Meta:
             model = Persona
             fields = '__all__'
     ```

8. **Admin de Django:**
   - Personalización y uso del panel de administración de Django.
   - Registro de modelos para gestionar datos a través del admin.
     ```python
     # admin.py
     from django.contrib import admin
     from .models import Persona

     admin.site.register(Persona)
     ```

