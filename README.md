# 🌿 Jardín Botánico Tulum

Sistema web para la gestión de un jardín botánico con generación de códigos QR que permiten a los visitantes consultar información de plantas en tiempo real.

---

## 🧠 Descripción del proyecto

Este sistema está dividido en dos partes principales:

* 🔐 **Administrador:** gestiona las plantas (crear, editar, eliminar) (admin) (contraseña : 1234)
* 📱 **Usuario:** consulta información escaneando códigos QR

Cada planta registrada genera un acceso único mediante URL con ID, el cual puede ser convertido en código QR.

---

## 🔄 Flujo del sistema

```plaintext
index.html (presentación del proyecto)
        ↓
login.html (acceso administrador)
        ↓
admin.html (gestión de plantas)
        ↓
Base de datos (SQLite)
        ↓
Generación de QR por planta
        ↓
QR → planta.html?id=XX
        ↓
Visualización de información de la planta
```

---

## 🚀 Cómo ejecutar el proyecto

### 1. Clonar o descargar el repositorio

```bash
git clone https://github.com/Cizco-2005/jardin-botanico-tulum.git
cd jardin-botanico-tulum
```

---

### 2. Instalar dependencias

```bash
npm install
```

---

### 3. Ejecutar el servidor

```bash
node server.js
```

---

### 4. Abrir en navegador

```bash
http://localhost:3000
```

---

## 🔐 Acceso administrador

Desde el index:

👉 Click en **Acceso Administrador**

O directamente:

```bash
http://localhost:3000/login.html
```

---

## 📱 Uso con códigos QR

Cada planta se puede consultar mediante una URL como:

```bash
http://localhost:3000/planta.html?id=16
```

Este enlace puede convertirse en código QR.

### Flujo del usuario:

1. Escanea el QR
2. Se abre la página de la planta
3. Visualiza:

   * Nombre
   * Descripción
   * Imagen
   * Ubicación
   * Galería

---

## 📁 Estructura del proyecto

```plaintext
css/
js/
assets/
data/
qrs/
uploads/

index.html
login.html
admin.html
planta.html
plantas.html
recuperar.html
Ubicacion.html
Galeria.html

server.js
package.json
package-lock.json

jardin_botanico.db
```

---

## ⚠️ Notas importantes

* El proyecto utiliza **Node.js + Express**
* La base de datos es **SQLite**
* GitHub **NO ejecuta el servidor automáticamente**
* Para que funcione, es necesario correr `node server.js`

---

## 🌐 Acceso desde dispositivos móviles (QR)

Para pruebas en red local:

```bash
http://IP-DE-TU-PC:3000/planta.html?id=XX
```

Ejemplo:

```bash
http://192.168.100.14:3000/planta.html?id=16
```

---

## 👨‍💻 Autor

Proyecto académico — Ingeniería de Software
Sistema de Jardín Botánico con QR

---

## 📄 Licencia

MIT License
