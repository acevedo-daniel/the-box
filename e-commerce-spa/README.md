# THE BOX - E-Commerce SPA

SPA minimalista y moderna para gestión y compra de productos de hardware, conectada a la API RESTful de THE BOX.

## 🚀 Tecnologías
- React + Vite
- JavaScript (100% en inglés)
- Estilo dark/minimalista, responsivo y profesional

## 🖥️ Instalación y ejecución

1. **Clona el repositorio y entra a la carpeta:**
   ```sh
   git clone <url-del-repo>
   cd e-commerce-spa
   ```

2. **Instala las dependencias:**
   ```sh
   npm install
   ```

3. **Configura la URL de la API:**
   - Por defecto, la SPA espera que la API corra en `http://localhost:5249`.
   - Si cambias el puerto de la API, edita `src/api/products.js`, `src/api/qr.js`, etc. y cambia la constante `API_URL`.

4. **Ejecuta la SPA:**
   ```sh
   npm run dev
   ```
   - Accede a [http://localhost:5173](http://localhost:5173)

## 📝 Configuración requerida

- **URL de la API:**  
  Cambiar el valor de `API_URL` en los archivos de servicios si la API corre en otro puerto o máquina.
- **CORS:**  
  Asegurarse de que la API permita el origen de la SPA (ver `AllowedOrigins` en `appsettings.json` de la API).
- **Credenciales:**  
  Usar su propio usuario para login o registro.
- **SMTP:**  
  Si quiere probar recuperación de contraseña, debe configurar SMTP en la API.

## 🧩 Funcionalidades principales

- Login, registro y recuperación de contraseña
- Listado, detalle, creación y edición de productos
- Filtros y paginación
- Gestión de categorías
- Generación y validación de QR para acceso exclusivo (BOX CLUB)
- Página de bienvenida exclusiva tras validar QR
- Diseño dark/minimalista, coherente en todas las páginas

## 👨‍💻 Créditos
- SPA desarrollada por Acevedo Mario Daniel y Alan Quenardelle (Universidad Tecnológica Nacional UTN)

## 📄 Licencia
Uso académico.
