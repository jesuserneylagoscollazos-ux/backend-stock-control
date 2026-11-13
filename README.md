# STOCK CONTROL

Sistema automatizado que interconecta modulos independientes para centralizar y relacionar la gestión de **ventas, contratos y bancos**, integrando todas sus funcionalidades en un flujo de trabajo. Diseñado con la **seguridad como prioridad**, garantiza la privacidad de cada área mediante un control de acceso repartido en roles **(admin y lector)** delimitando las capacidades y el alcance de cada usuario.

---

## 🛠️ Tecnologías Utilizadas

* **Entorno de ejecución:** [Node.js](https://nodejs.org) (v24.18.0)
* **Framework Backend:** [Express.js](https://expressjs.com)
* **Base de Datos:** PostgreSQL
* **ORM / ODM:** [Ej. Prisma / Sequelize / Mongoose] *(opcional)*
* **Otras herramientas:** [Ej. Dotenv, Cors, Morgan, etc.]

---

## 📋 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado en tu máquina local:

* **Node.js** v24.18.0 y **npm**.
* **Git** para clonar el repositorio.
* **PostgreSQL** instalado localmente o acceso a una instancia en la nube.

---

## 🚀 Instalación y Ejecución Local

Sigue estos pasos para levantar el proyecto en tu entorno de desarrollo:

### 1. Clonar el repositorio y entrar a la carpeta
```bash
git clone https://github.com/jesuserneylagoscollazos-ux/backend-stock-control.git
cd backend-stock-control
```

### 2. Instalar dependencias
Ejecuta el siguiente comando para instalar todos los paquetes necesarios:
```bash
npm install cors dotenv express morgan pg
```

### 3. Configurar variables de entorno
Crea un archivo llamado `.env` en la raíz de la carpeta `backend` (puedes copiar el contenido de `.env.example`) y configura tus credenciales:

```env
# Configuración del Servidor
PORT=3000
NODE_ENV=development

# Configuración de PostgreSQL
PG_HOST=localhost
PG_PORT=5432
PG_DATABASE=nombre_base_de_datos
PG_USER=postgres
PG_PASSWORD=contraseña_secreta

# Pools de conexiones
PG_MAX_POOL=10
PG_IDLE_TIMEOUT=30000
```

### 4. Ejecutar el proyecto
Para iniciar el servidor en modo desarrollo:
```bash
npm run dev
```
O para iniciar en modo producción:
```bash
npm start
```
El servidor estará corriendo en `http://localhost:3000` (puedes verificar su estado en el endpoint de salud configurado en `healthRoutes.js`).

---

## 📁 Estructura de Carpetas

```text
backend/
├── node_modules/           # Dependencias instaladas del proyecto
├── src/                    # Código fuente principal de la aplicación
│   ├── config/             # Archivos de configuración general
│   │   ├── db.js           # Conexión y configuración de la base de datos
│   │   └── environment.js  # Gestión y exportación de variables de entorno
│   ├── controllers/        # Lógica de negocio y manejo de peticiones/respuestas
│   │   └── healthController.js # Controlador para verificar el estado del servidor
│   ├── routes/             # Definición de endpoints y rutas de la API
│   │   └── healthRoutes.js # Rutas para el monitoreo de salud (health check)
│   ├── app.js              # Configuración principal de Express y middlewares
│   └── server.js           # Punto de entrada que levanta el servidor HTTP
├── .env                    # Variables de entorno locales (ignorado por Git)
├── .env.example            # Plantilla de ejemplo para las variables de entorno
├── .gitignore              # Archivos y carpetas excluidos del control de versiones
├── package-lock.json       # Registro exacto de las versiones de dependencias
├── package.json            # Metadatos, scripts y dependencias del proyecto
└── README.md               # Documentación principal del proyecto
```

---

## 👥 Desarrollador

* **Jesús Erney Lagos Collazos** - [@jesuserneylagoscollazos-ux](https://github.com/jesuserneylagoscollazos-ux)
