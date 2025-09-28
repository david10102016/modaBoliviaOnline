Descripción
Moda Bolivia es una tienda de ropa online desarrollada con Flask (Python), SQLite y Bootstrap. Este proyecto es una solución completa para la venta de ropa en Santa Cruz de la Sierra, Bolivia, con funcionalidades como catálogo de productos, carrito de compras, sistema de login/registro, moderación de comentarios, y un tour guiado con Driver.js. Incluye un sistema de Prueba de Usuario (UAT) para evaluar la usabilidad.
El proyecto se enfoca en una experiencia de usuario intuitiva, con énfasis en categorías para hombres, mujeres, niños y ofertas especiales. Ubicado en Equipetrol, Santa Cruz, el sitio simula un flujo de compra real con métodos de pago locales (Tigo Money, QR Simple, WhatsApp).
Características Principales

Catálogo de Productos: Organizado por categorías con imágenes y descripciones.
Carrito de Compras: Agrega, actualiza y elimina productos; soporta sesiones de usuario y anónimas.
Sistema de Usuarios: Login/registro con validaciones (email, teléfono boliviano, contraseña segura).
Comentarios y Moderación: Usuarios logueados pueden comentar productos; comentarios con ≤3 estrellas van a moderación para el admin.
Tour Guiado y UAT: Driver.js para tours interactivos; sistema UAT con timer de inactividad para feedback de usabilidad.
Checkout Boliviano: Soporte para métodos de pago locales y facturación (NIT, CI).
Panel Administrativo: Gestión de productos, órdenes y comentarios pendientes.
Responsive Design: Bootstrap para dispositivos móviles.

Instalación
Requisitos

Python 3.8+
SQLite (incluido en Python)
Bibliotecas: Flask, bcrypt, werkzeug, sqlite3 (instala con pip install flask bcrypt werkzeug).

Pasos

Clona el Repositorio:
textgit clone <tu-repo-url>
cd tienda-ropa-online

Instala Dependencias:
textpip install -r requirements.txt
(Crea requirements.txt con: flask==2.3.3, bcrypt==4.1.2, werkzeug==2.3.7).
Configura la Base de Datos:

Ejecuta python database.py para inicializar tienda.db.
Opcional: python init_db.py para poblar datos de prueba.


Ejecuta la Aplicación:
textpython app.py

Abre http://127.0.0.1:5000 en tu navegador.


Credenciales de Prueba:

Admin: Email admin@modabolivia.com, Contraseña Admin123!.
Usuario: Email usuario@modabolivia.com, Contraseña Usuario123!.



Uso
Para Clientes

Navegar: Explora categorías en el menú o busca productos.
Comprar: Agrega al carrito, ve a /carrito, y completa el checkout.
Comentar: Inicia sesión y comenta en productos (calificación 1-5).
Tour: Haz clic en "Tour" para guía interactiva.

Para Administrador

Inicia sesión con credenciales admin.
Accede a /admin para estadísticas, productos y órdenes.
Moderación: Ve a /moderar para aprobar comentarios pendientes.

UAT (Prueba de Usuario)

Haz clic en "Tour" > "Prueba UAT".
Selecciona un escenario y navega. La notificación de feedback aparece tras 25 segundos de inactividad.

Estructura del Proyecto
texttienda-ropa-online/
├── app.py                 # Aplicación Flask principal
├── database.py            # Configuración de SQLite y funciones de BD
├── init_db.py             # Poblamiento inicial de datos
├── static/
│   ├── css/
│   │   └── custom.css     # Estilos personalizados
│   ├── js/
│   │   ├── custom.js      # JavaScript principal (tours, UAT, interacciones)
│   │   └── driver-simple.js # Driver.js local para tours
│   └── images/
│       └── productos/     # Imágenes de productos por categoría
├── templates/
│   ├── base.html          # Plantilla base
│   ├── index.html         # Página principal
│   ├── login.html         # Login y registro
│   ├── admin.html         # Panel admin
│   ├── moderar.html       # Moderación de comentarios
│   └── ... (otras plantillas)
└── requirements.txt       # Dependencias Python
Contribuciones
Contribuciones son bienvenidas. Por favor, abre un issue o pull request en GitHub.
Licencia
MIT License - Ver LICENSE para detalles.
Autor
Juan David Uscamayta Ramos
Desarrollador Full Stack
YouTube: @jdav777
Email: jdav777@outlook.com
Santa Cruz de la Sierra, Bolivia
Contacto

WhatsApp: 
Canal de YouTube: JD Server para tutoriales y actualizaciones.
