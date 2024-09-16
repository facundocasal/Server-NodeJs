# Backend CRUD de Productos con Chat y Manejo de Imágenes

Este es un proyecto de backend desarrollado con **Node.js**, que implementa un **CRUD de productos** permitiendo agregar, actualizar, eliminar y listar productos. También cuenta con un **chat** en tiempo real utilizando **Socket.IO**, manejo de imágenes con **Multer**, y gestión de usuarios y sesiones utilizando **JWT** (JSON Web Tokens) para autenticación. Para la base de datos se utiliza **MongoDB**.

## Características

- CRUD completo de productos (Crear, Leer, Actualizar, Eliminar).
- Gestión de usuarios: registro, inicio de sesión y manejo de sesiones utilizando **JWT** (JSON Web Tokens).
- Integración con MongoDB utilizando Mongoose para la gestión de la base de datos.
- Implementación de autenticación con **JWT** para proteger rutas y recursos.
- Carga y manejo de imágenes usando **Multer**.
- Chat en tiempo real utilizando **Socket.IO**.
- Manejo de peticiones HTTP con **Express**.
- Seguridad con **bcrypt** para el manejo de contraseñas.
- Control de CORS con la librería **cors**.
- Validación de datos de entrada con **express-validator**.

## Requisitos

Asegúrate de tener instalados los siguientes requisitos:

- **Node.js** v14.x o superior
- **MongoDB** (puedes usar un servidor local o una instancia en la nube como MongoDB Atlas)

## Instalación

1. Clona este repositorio:

   ```bash
   git clone https://github.com/facundocasal/Server-NodeJs.git

2. Entra en el directorio del proyecto:
   
   ```bash
    cd Server-NodeJs

4. Instala las dependencias:

   ```bash
   npm install
   
5. Crea un archivo .env en la raíz del proyecto con las siguientes variables de entorno:

   ```bash
   MONGO_URI=<tu-url-de-mongodb>
   JWT_SECRET=<tu-secreto-jwt>
   PORT=<puerto-del-servidor>
   
6. Ejecuta el servidor en modo desarrollo:

   ```bash
   npm run dev
   
  O en modo producción utilizando "npm start"

## Endpoints

### CRUD de Productos

  ### Productos 

- **GET** `/product/` - Listar todos los productos.
- **POST** `/product/createProduct/` - Crear un nuevo producto.
- **POST** `/product/updateProduct/` - Actualizar un producto existente (el ID del producto se recibe en el cuerpo de la solicitud `req.body`).
- **DELETE** `/product/deleteProduct/` - Eliminar un producto (el ID del producto se recibe en el cuerpo de la solicitud `req.body`).

  ### Usuarios 

- **GET** `/users/register` - Obtener vista para registrarse.
- **GET** `/users/login` - Obtener vista para iniciar sesion de usuario.
- **GET** `/users/panel` - Obtener informacion del usuario.
- **GET** `/users/logOut` - Cerrar sesion.
- **POST** `/users/register` - Registrar nuevo usuario.
- **POST** `/users/login` - Iniciar sesion de usuario.

  ### Carrito 

- **GET** `/cart/` - Obtener carritos del usuario.
- **POST** `/cart/:id` - Obtener carrito del usuario por id.
- **POST** `/cart/:cartId/:prodId` - Obtener un producto del carrito.

    ### Ordenes
  
- **POST** `/orders/send'` - Crear orden de compra.


### Chat (Socket.IO)

El chat está integrado con **Socket.IO**. Los clientes pueden conectarse y enviar mensajes en tiempo real.

### Manejo de Imágenes

Las imágenes pueden ser cargadas y manejadas usando **Multer**.

## Dependencias

El proyecto utiliza las siguientes dependencias:

- **axios**: "^1.1.3"
- **bcrypt**: "^5.1.0"
- **compression**: "^1.7.4"
- **cookie-parser**: "~1.4.4"
- **cors**: "^2.8.5"
- **debug**: "~2.6.9"
- **dotenv**: "^16.0.3"
- **ejs**: "~2.6.1"
- **express**: "~4.16.1"
- **express-jwt**: "^7.7.7"
- **express-validator**: "^6.14.2"
- **http-errors**: "~1.6.3"
- **jsonwebtoken**: "^8.5.1"
- **mongoose**: "^6.7.2"
- **morgan**: "~1.9.1"
- **multer**: "^1.4.5-lts.1"
- **nodemailer**: "^6.8.0"
- **nodemon**: "^2.0.20"
- **socket.io**: "^4.5.3"
- **yargs**: "^17.6.2"

## Contribuciones

Las contribuciones son bienvenidas. Si tienes alguna sugerencia o mejora, por favor abre un issue o envía un pull request.
