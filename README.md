# 🛍️ Milaccesorios – Sistema de Gestión Básico

**Milaccesorios** es una empresa dedicada a la fabricación de bisutería artesanal.  
Este proyecto es un sistema de gestión interno que permite administrar **productos**, **inventario** y **pedidos**, desarrollado en **Node.js** con **Vue.js**.

---

## 📋 Características

- Gestión de productos (crear, editar, eliminar, listar).
- Control básico de inventario.
- Registro y seguimiento de pedidos.
- Acceso restringido mediante login.
- Interfaz web responsive con Vue.js y Bootstrap.

---

## 🛠️ Tecnologías

- **Frontend:** Vue.js 3, Bootstrap 5
- **Backend:** Node.js, Express.js
- **Base de Datos:** MongoDB
- **Control de Versiones:** Git/GitHub

---

## 📦 Requisitos Previos

Asegúrate de tener instalado:

- [Node.js](https://nodejs.org/) (v18 o superior)
- [npm](https://www.npmjs.com/) o [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) (local o en la nube con MongoDB Atlas)

---

## 🚀 Instalación y Ejecución

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/tuusuario/milaccesorios.git
   cd milaccesorios
````

2. **Instalar dependencias del backend**

   ```bash
   cd backend
   npm install
   ```

3. **Instalar dependencias del frontend**

   ```bash
   cd ../frontend
   npm install
   ```

4. **Configurar variables de entorno**

   * En la carpeta `backend`, crear un archivo `.env` con:

     ```env
     PORT=4000
     MONGODB_URI=mongodb://localhost:27017/milaccesorios
     JWT_SECRET=TuClaveSecreta
     ```

5. **Ejecutar el backend**

   ```bash
   cd backend
   npm run dev
   ```

6. **Ejecutar el frontend**

   ```bash
   cd frontend
   npm run serve
   ```

7. **Abrir en el navegador**

   ```
   http://localhost:8080
   ```

---

## 📂 Estructura del Proyecto

```
milaccesorios/
│
├── backend/                # API REST con Node.js y Express
│   ├── src/
│   │   ├── models/         # Modelos de MongoDB
│   │   ├── routes/         # Rutas API
│   │   ├── controllers/    # Lógica de negocio
│   │   └── app.js
│   └── package.json
│
├── frontend/               # Interfaz web con Vue.js
│   ├── src/
│   │   ├── components/     # Componentes Vue
│   │   ├── views/          # Vistas
│   │   ├── router/         # Rutas de la app
│   │   └── main.js
│   └── package.json
│
└── README.md
```

---

## 🧪 Scripts útiles

**Backend**

```bash
npm run dev   # Ejecuta el backend en modo desarrollo
npm start     # Ejecuta el backend en producción
```

**Frontend**

```bash
npm run serve # Ejecuta el frontend en desarrollo
npm run build # Construye la versión de producción
```

---

## 🤝 Contribuir

1. Haz un **fork** del proyecto.
2. Crea una rama para tu nueva funcionalidad:

   ```bash
   git checkout -b mi-nueva-funcionalidad
   ```
3. Realiza tus cambios y haz commit:

   ```bash
   git commit -m "Agrego nueva funcionalidad"
   ```
4. Envía tus cambios con un **Pull Request**.

---

## 📜 Licencia

Este proyecto se distribuye bajo la licencia MIT.
Consulta el archivo [LICENSE](LICENSE) para más detalles.

```
