# Tienda Online UMA

Aplicación web desarrollada con Python, Flask y PostgreSQL como proyecto académico. El sistema permite administrar un catálogo de productos físicos, digitales y perecibles, gestionar usuarios por roles y realizar compras mediante un carrito.

🚀 Características
Registro e inicio de sesión de usuarios.
Contraseñas almacenadas de forma segura mediante hash.
Sistema de roles:
Administrador: crear, editar y desactivar productos.
Cliente: consultar productos y utilizar el carrito.
CRUD de productos.
Tipos de productos:
📦 Físicos
💻 Digitales
🍓 Perecibles
Cálculo de precios mediante polimorfismo.
Carrito de compras almacenado en la sesión.
Subida de imágenes para los productos.
Imágenes almacenadas en static/uploads/.
Imagen predeterminada para productos sin fotografía.
Validación de archivos de imagen.
Límite de tamaño para las imágenes.
Control de acceso mediante decoradores personalizados.
Mensajes de éxito y error mediante flash().
Diseño responsive utilizando Bootstrap.
Interfaz personalizada mediante CSS.
🛠️ Tecnologías utilizadas
Python 3
Flask
Flask-SQLAlchemy
PostgreSQL
HTML5
CSS3
Bootstrap 5
Jinja2
Werkzeug
Git / GitHub
📁 Estructura del proyecto
tienda_online_uma/
│
├── app.py
├── auth.py
├── config.py
├── models.py
├── init_db.py
├── requirements.txt
├── .gitignore
│
├── static/
│   ├── style.css
│   └── uploads/
│
└── templates/
    ├── base.html
    ├── index.html
    ├── detalle.html
    ├── editar.html
    ├── login.html
    ├── registro.html
    ├── carrito.html
    ├── nuevo_fisico.html
    ├── nuevo_digital.html
    └── nuevo_perecible.html
⚙️ Instalación

Clona el repositorio:

git clone URL_DEL_REPOSITORIO

Entra en la carpeta:

cd tienda_online_uma

Crea el entorno virtual:

python -m venv venv

En Windows, actívalo con:

venv\Scripts\activate

Instala las dependencias:

pip install -r requirements.txt
🗄️ Configuración de PostgreSQL

Crea la base de datos:

tienda_online_uma

Configura las variables de entorno en un archivo .env:

DB_USER=postgres
DB_PASSWORD=TU_CONTRASEÑA
DB_HOST=localhost
DB_PORT=5432
DB_NAME=tienda_online_uma
SECRET_KEY=TU_SECRET_KEY

El archivo .env no debe subirse al repositorio.

▶️ Ejecutar la aplicación

Activa el entorno virtual:

venv\Scripts\activate

Ejecuta Flask:

python app.py

Después abre:

http://127.0.0.1:5000
👤 Roles
Administrador

El administrador puede:

Crear productos físicos, digitales y perecibles.
Editar productos.
Desactivar productos.
Subir y cambiar imágenes.
Acceder al panel de administración.
Cliente

El cliente puede:

Consultar el catálogo.
Ver detalles de productos.
Agregar productos al carrito.
Consultar el carrito.
Eliminar productos del carrito.
🖼️ Imágenes

Las imágenes de los productos se almacenan en:

static/uploads/

El sistema permite utilizar archivos:

PNG
JPG
JPEG
GIF
WEBP

Las imágenes se renombran automáticamente para evitar conflictos entre archivos.

🔐 Seguridad

El proyecto utiliza decoradores personalizados para controlar el acceso:

@login_requerido

y:

@rol_requerido("admin")

De esta manera, las rutas administrativas no pueden ser utilizadas por usuarios que no tengan los permisos correspondientes.

📱 Diseño

La interfaz utiliza Bootstrap para obtener un diseño adaptable a computadoras, tablets y teléfonos móviles.

También se incluye un archivo CSS personalizado para:

Tarjetas de productos.
Espaciado.
Colores de la marca.
Botones.
Imágenes.
Navbar.
Footer.
Diseño responsive.
🎓 Proyecto académico

Tienda Online UMA es un proyecto académico desarrollado para aplicar conceptos de:

Programación web con Flask.
Bases de datos.
PostgreSQL.
POO y polimorfismo.
Autenticación y autorización.
Manejo de sesiones.
Subida y gestión de archivos.
Diseño web responsive.
Control de versiones con Git y GitHub.
