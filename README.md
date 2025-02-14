# 📝 Proyecto de Tareas con Express, Vue y Cypress

Este es un proyecto de gestión de tareas con **Node.js (Express)** en el backend, **Vue.js** en el frontend y pruebas **E2E con Cypress**.

## 📌 Estructura del Proyecto
```
/ejemplotareasBackEndExpress  # Backend (Node.js + Express)
│── db/                      # Configuración de base de datos
│── routes/                  # Rutas del servidor
│── server.js                # Servidor principal
│── config.env               # Variables de entorno (añadir en .gitignore)
│── package.json             # Dependencias del backend
│── Dockerfile               # Configuración para Docker
│── README.md                # Documentación del backend
│
/ejemplotareasFrontEnd       # Frontend (Vue + Vuetify)
│── src/                     # Código fuente de Vue.js
│── public/                  # Archivos estáticos
│── cypress/                 # Pruebas E2E con Cypress
│── package.json             # Dependencias del frontend
│── Dockerfile               # Configuración para Docker
│── README.md                # Documentación del frontend
```

---

## 🚀 **Cómo ejecutar el Backend (Node.js + Express)**

### 📌 **1. Instalar dependencias**
```bash
cd back/ejemplotareasBackEndExpress
npm install
```

### 📌 **2. Configurar variables de entorno (`config.env`)**
Crear el archivo `config.env` en `/back/ejemplotareasBackEndExpress` con el siguiente contenido:

```plaintext
PORT=3000
MONGO_URL=mongodb+srv://<usuario>:<password>@cluster.mongodb.net/ejemplo?retryWrites=true&w=majority
```
⚠ **Reemplazar `<usuario>` y `<password>` por los datos correctos de MongoDB Atlas.**

### 📌 **3. Ejecutar el backend**
```bash
npm start
```
El servidor debería ejecutarse en `http://localhost:3000/`

---

## 🎨 **Cómo ejecutar el Frontend (Vue.js + Vuetify)**

### 📌 **1. Instalar dependencias**
```bash
cd front/ejemplotareasfrontend
npm install
```

### 📌 **2. Configurar variables de entorno (`.env`)**
Crear el archivo `.env` en `/front/ejemplotareasfrontend` con el siguiente contenido:

```plaintext
VUE_APP_BACKEND_URL=http://localhost:3000
```

### 📌 **3. Ejecutar el frontend**
```bash
npm run serve
```
El frontend debería ejecutarse en `http://localhost:8081/`

---

## 🧪 **Ejecutar Pruebas E2E con Cypress**

### 📌 **1. Abrir Cypress UI**
```bash
cd front/ejemplotareasfrontend
npx cypress open
```
Seleccionar **"E2E Testing"**, elegir un navegador y ejecutar las pruebas.

### 📌 **2. Ejecutar pruebas en la terminal**
```bash
npx cypress run
```

---

## 📦 **Docker (Opcional)**
Para ejecutar el proyecto en **Docker**, usar:

```bash
docker-compose up --build
```

---

## 🔥 **Notas Adicionales**
- **Revisar los logs en caso de errores** (`npm start` en backend y `npm run serve` en frontend).
- **Si MongoDB no está configurado en Atlas**, usar una base de datos local con `mongodb://localhost:27017/ejemplo`.
- **Las pruebas Cypress están en `cypress/e2e/`**.

---

## 🎯 **Autores**
- **Bazurtorivadeneyra Einoso**  
- **Colaboradores:** Equipo de desarrollo

🚀 _¡Listo para desplegar y probar!_ 🚀
