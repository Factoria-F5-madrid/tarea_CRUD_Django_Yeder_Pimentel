# 🧠 Preguntas sobre Django, CRUD y Arquitectura de Software

---

## 1️⃣ ¿Qué es un CRUD y cuál es su propósito en el desarrollo de aplicaciones web?

🔄 **CRUD** es el acrónimo de las 4 operaciones básicas sobre una base de datos:

- 🟢 **Create (Crear)**
- 🔵 **Read (Leer)**
- 🟠 **Update (Actualizar)**
- 🔴 **Delete (Eliminar)**

📌 **Propósito**: Facilita la gestión de información entre la interfaz del usuario y la base de datos.

---

## 2️⃣ ¿Qué son los patrones de arquitectura en desarrollo de software?

🧱 Son estructuras reutilizables que organizan el código para hacerlo más:

- 📈 Escalable
- 🔧 Mantenible
- 👁️‍🗨️ Legible

### 🧩 ¿Qué es el patrón MVC (Modelo–Vista–Controlador)?

- 📦 **Modelo**: Representa los datos y la lógica de negocio.
- 🧠 **Vista**: Contiene la lógica que recibe las peticiones del usuario y devuelve respuestas.
- 🕹️ **Controlador**: Coordina las acciones entre el modelo y la vista.

### 🧩 ¿Qué es el patrón MVT (Modelo–Vista–Template)?

- 📦 **Modelo**: Representa los datos y lógica de negocio.
- 🧠 **Vista**: Recibe peticiones y devuelve respuestas.
- 🖼️ **Template**: Define cómo se muestra la información al usuario (HTML).

### ⚖️ Diferencias entre MVC y MVT:

| Elemento    | MVC                   | MVT                             |
| ----------- | --------------------- | ------------------------------- |
| Vista       | Lógica + presentación | Solo lógica (View en Django)    |
| Template    | No existe como tal    | Sí (HTML con lógica)            |
| Controlador | Independiente         | Lo gestiona Django internamente |

### ✅ ¿Cuál se usa en Django?

🎯 **MVT (Modelo–Vista–Template)**

---

## 3️⃣ ¿Cómo se estructura un proyecto en Django?

📁 Un proyecto Django se compone de apps con la siguiente estructura típica:

- `models.py` → Define las estructuras de datos (tablas).
- `views.py` → Contiene la lógica para manejar peticiones.
- `templates/` → Contiene archivos HTML para la interfaz del usuario.
- `urls.py` → Define las rutas que conectan URLs con vistas.

### 🧠 ¿Para qué se usa `{% %}` y `{{ }}` en templates?

- `{{ variable }}` → Muestra datos dinámicos (por ejemplo, `{{ nombre }}`).
- `{% tag %}` → Controla la lógica del template (por ejemplo: `{% if %}`, `{% for %}`, `{% url %}`).

---

## 4️⃣ ¿Cuál es el flujo de datos entre un formulario HTML y la base de datos en Django?

1. 📝 El usuario rellena un formulario en HTML.
2. 📤 El formulario se envía por `POST` a una URL.
3. 📬 Django recibe la petición en una vista.
4. ✅ La vista valida y guarda los datos usando un modelo o `ModelForm`.
5. 🗃️ Los datos se guardan en la base de datos.
6. 📄 La vista responde con un `template` actualizado o redirige.

---

## 5️⃣ ¿Qué herramientas o comandos ofrece Django para facilitar el desarrollo de un CRUD?

🔧 Django facilita el desarrollo de operaciones CRUD con las siguientes herramientas y comandos:

### 🔍 ¿Para qué sirve cada uno?

- 📦 `startapp` → Crea una nueva aplicación Django.
- 🛠️ `makemigrations` → Genera archivos de migración según los modelos.
- 🧱 `migrate` → Aplica las migraciones a la base de datos.
- 🚀 `runserver` → Inicia el servidor local de desarrollo.
- 📝 `ModelForm` → Genera formularios automáticamente desde modelos.
- 🧑‍💼 `admin` → Panel gráfico para gestionar modelos fácilmente.
- 🔐 `createsuperuser` → Crea un usuario administrador para acceder al panel de administración.

### 🧰 Otros comandos útiles

- 🐚 `shell` → Abre consola interactiva de Python con acceso a los modelos.
- 📥 `loaddata` / 📤 `dumpdata` → Importa y exporta datos en formato JSON.
- 📦 `collectstatic` → Recolecta archivos estáticos para producción.
- 🧪 `test` → Ejecuta tests del proyecto.

---

## 6️⃣ ¿Cómo funciona el Admin de Django?

🧑‍💻 El **Admin de Django** es una interfaz web lista para usar que permite administrar fácilmente los modelos registrados.

### 📘 Funcionamiento del Admin – Formato `README.md`

````markdown
# 🛠️ Django Admin Panel

El **Admin de Django** es una interfaz web automática y personalizable que permite gestionar los datos de la aplicación fácilmente.

## 🚀 ¿Qué puedes hacer con el admin?

- 📄 Ver, agregar, editar y eliminar registros de cualquier modelo.
- 👥 Administrar usuarios, grupos y permisos.
- 🔍 Buscar y filtrar registros.
- 🖼️ Personalizar la visualización de modelos.

## ⚙️ ¿Cómo se activa?

1. **Crear un superusuario**:
   ```bash
   python manage.py createsuperuser
   ```
````
