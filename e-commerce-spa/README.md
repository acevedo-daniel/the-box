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
   - Si tu compañero usa otro puerto, debe editar `src/api/products.js`, `src/api/qr.js`, etc. y cambiar la constante `API_URL`.

4. **(Opcional) Configura el proxy de Vite:**
   - Si la API corre en otro puerto, edita `vite.config.js`:
     ```js
     server: {
       proxy: {
         '/api': 'http://localhost:5249'
       }
     }
     ```

5. **Ejecuta la SPA:**
   ```sh
   npm run dev
   ```
   - Accede a [http://localhost:5173](http://localhost:5173)

## 📝 Cosas que debe modificar tu compañero

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

## 👨‍💻 Desarrollo

- Todo el código está en inglés.
- El diseño sigue la línea minimalista, sin elementos innecesarios.
- La navegación es fluida y coherente.

---

## 📄 README revisado para `/e-commerce-api`

El README de la API ya está muy completo y actualizado.  
Solo asegúrate de que tu compañero:

- **Configure correctamente `appsettings.json`:**
  - Cadena de conexión a SQL Server.
  - Credenciales SMTP para envío de emails.
  - `AllowedOrigins` para permitir la URL de la SPA.

- **Use los comandos:**
  ```sh
  dotnet restore
  dotnet ef database update --project e-commerce-api.csproj
  dotnet run --project e-commerce-api.csproj
  ```

- **Verifique el puerto de la API** (por defecto, 5249) y lo configure igual en la SPA.

- **Pruebe los endpoints con Swagger** en [http://localhost:5249/swagger](http://localhost:5249/swagger).

---

¿Quieres que agregue alguna sección extra (por ejemplo, troubleshooting, screenshots, o pasos para producción)? ¿O necesitas el README en inglés?

---

## 📦 Estructura recomendada del repositorio

```
the-box/
│
├── e-commerce-api/      # Backend ASP.NET Core
│   └── ...              # (todo el código, configs, NOTAS.md, etc.)
│
├── e-commerce-spa/      # Frontend React + Vite
│   └── ...              # (todo el código, configs, README.md, etc.)
│
├── README.md            # (opcional, guía general del proyecto)
└── .gitignore           # (puedes tener uno global o por carpeta)
```

---

## 🚀 ¿Cómo subirlo a un solo repo?

1. **Ubica ambas carpetas dentro de una carpeta raíz** (por ejemplo, `the-box`).
2. Abre una terminal en esa carpeta raíz.
3. Inicializa el repositorio:
   ```sh
   git init
   git add .
   git commit -m "Initial commit: API and SPA"
   ```
4. Crea el repo en GitHub (o tu plataforma preferida).
5. Agrega el remoto y sube:
   ```sh
   git remote add origin <URL-del-repo>
   git push -u origin main
   ```

---

## ✅ Ventajas de un solo repo

- Más fácil de clonar y mantener.
- Documentación y scripts compartidos.
- Menos confusión para tu compañero.

---

## ⚠️ ¿Cuándo usar repos separados?
- Solo si los proyectos van a evolucionar de forma independiente o los va a mantener equipos distintos.
- Si tienes requisitos de despliegue muy diferentes.

---

**Recomendación:**  
¡Sube todo junto en un solo repo!  
Incluye un README general en la raíz explicando la estructura y los pasos básicos.

¿Quieres que te ayude a armar ese README general o necesitas un `.gitignore` recomendado?
