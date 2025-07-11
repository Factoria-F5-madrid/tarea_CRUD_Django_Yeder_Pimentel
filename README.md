# 🧠 Preguntas sobre Django, CRUD y Arquitectura de Software

## 1. ¿Qué es un CRUD y cuál es su propósito en el desarrollo de aplicaciones web?

- CRUD es el acrónimo que representa las 4 operaciones básicas que se realizan sobre los datos en una BBDD : CREAR (Create), LEER (Read), ACTUALIZAR(Update) y BORRAR (Delete).
  Propósito: Facilita la gestión de información desde la interfaz de usuario hacia la base de datos y viceversa.

---

## 2. ¿Qué son los patrones de arquitectura en desarrollo de software?

- Son estructuras reutilizables que organizan el código de una aplicación para hacerlo más escalable, mantenible y legible.

- ¿Qué es el patrón MVC (Modelo–Vista–Controlador)?

- **Modelo**: representa los datos y la lógica de negocio.
- **Vista**: contiene la lógica que recibe las peticiones del usuario y devuelve respuestas.
- **Controlador**: recibe las solicitudes del usuario y coordina el modelo y la vista.

- ¿Qué es el patrón MVT (Modelo–Vista–Template)?

- **Modelo**: representa los datos y lógica de negocio.
- **Vista**: contiene la lógica que recibe peticiones y devuelve respuestas.
- **Template**: define cómo se muestra la información al usuario (HTML)

- ¿Cuáles son las diferencias entre MVC y MVT?

| Elemento    | MVC                   | MVT                            |
| ----------- | --------------------- | ------------------------------ |
| Vista       | Lógica + presentación | Lógica (View en Django)        |
| Template    | No existe como tal    | Sí, HTML con lógica            |
| Controlador | Controlador separado  | Framework lo gestiona (Django) |

- ¿Cuál de estos dos patrones se usa en Django?

--- MVT (Modelo–Vista–Template)

## 3. ¿Cómo se estructura un proyecto en Django?

- Un proyecto Django se compone de apps que tienen esta estructura típica:

- models.py: define las estructuras de datos (tablas de base de datos).

- views.py: maneja la lógica de las peticiones.

- templates/: contiene los archivos HTML que ve el usuario.

- urls.py: define las rutas que conectan URLs con vistas.

- ¿Para qué se usa el signo `{% %}` en los templates?

- **{{ variable }}** : se usa para mostrar datos dinámicos (por ejemplo, {{ nombre }}).
- **{% tag %}**: se usa para lógica del template (por ejemplo, {% if %}, {% for %}, {% url %}, etc.).

## 4. ¿Cuál es el flujo de datos entre un formulario HTML y la base de datos en Django?

--- El usuario rellena el formulario en HTML.

--- El formulario se envía por POST a una URL.

--- Django recibe la petición en una vista.

--- La vista valida y guarda los datos usando un modelo o un ModelForm.

--- Los datos se guardan en la base de datos.

--- La vista responde al usuario con un template HTML actualizado o redirecciona.

## 5. ¿Qué herramientas o comandos ofrece Django para facilitar el desarrollo de un CRUD?

Django ofrece una serie de comandos y herramientas que simplifican la creación y gestión de aplicaciones web con operaciones CRUD. A continuación se detallan las más importantes:

### ¿Para qué sirve cada uno?

- `startapp`  
  Crea una nueva aplicación Django dentro del proyecto. Cada app encapsula una funcionalidad concreta (por ejemplo, usuarios, productos, blog, etc.).

- `makemigrations`  
  Crea archivos de migración a partir de los cambios realizados en los modelos (definiciones de tablas en la base de datos).

- `migrate`  
  Aplica las migraciones pendientes a la base de datos, creando o actualizando las tablas y relaciones.

- `runserver`  
  Lanza el servidor de desarrollo de Django en `localhost:8000` por defecto para probar la aplicación.

- `ModelForm`  
  Una clase que genera automáticamente formularios HTML basados en modelos definidos. Facilita la validación y el guardado de datos del formulario.

- `admin`  
  Permite registrar modelos y gestionarlos desde una interfaz gráfica preconstruida. Muy útil para administración interna del sitio.

- `createsuperuser`  
  Crea un usuario administrador que puede acceder al panel de administración (`/admin`) y gestionar todos los modelos registrados.

- **Otros comandos útiles**:

  - `shell`: Abre una consola interactiva para manipular directamente los modelos y datos.
  - `loaddata` / `dumpdata`: Cargar y guardar datos en formato JSON (útil para backups y pruebas).
  - `collectstatic`: Recolecta archivos estáticos para servirlos en producción.
  - `test`: Ejecuta los tests unitarios del proyecto.

---

## 6. ¿Cómo funciona el Admin de Django?

El panel de administración de Django permite gestionar todos los modelos registrados a través de una interfaz gráfica web segura y lista para usar.

### Funcionamiento del admin – Formato `README.md`

````markdown
# 🛠️ Django Admin Panel

El **Admin de Django** es una interfaz web automática y personalizable que permite gestionar los datos de la aplicación fácilmente.

## 🚀 ¿Qué puedes hacer con el admin?

- Ver, agregar, editar y eliminar registros de cualquier modelo.
- Administrar usuarios, grupos y permisos.
- Buscar y filtrar registros fácilmente.
- Personalizar la visualización de los modelos en la interfaz.

## ⚙️ ¿Cómo se activa?

1. **Crear un superusuario**:
   ```bash
   python manage.py createsuperuser
   ```
````
