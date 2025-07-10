# THE BOX - E-Commerce Fullstack Project

Este repositorio contiene tanto el backend (API ASP.NET Core) como el frontend (SPA en React + Vite) para la plataforma THE BOX.

## 📦 Estructura del repositorio

```
the-box/
│
├── e-commerce-api/      # Backend ASP.NET Core
│   └── ...              # (código, configs, NOTAS.md, etc.)
│
├── e-commerce-spa/      # Frontend React + Vite
│   └── ...              # (código, configs, README.md, etc.)
│
├── README.md            # (este archivo)
└── .gitignore           # (global o por carpeta)
```

## 🚀 Instalación y ejecución

1. **Clona el repositorio:**
   ```sh
   git clone <url-del-repo>
   cd the-box
   ```

2. **Configura y ejecuta el backend (API):**
   ```sh
   cd e-commerce-api
   # Edita appsettings.json con tu cadena de conexión y SMTP
   dotnet restore
   dotnet ef database update --project e-commerce-api.csproj
   dotnet run --project e-commerce-api.csproj
   # La API corre por defecto en http://localhost:5249
   ```

3. **Configura y ejecuta el frontend (SPA):**
   ```sh
   cd ../e-commerce-spa
   npm install
   npm run dev
   # La SPA corre por defecto en http://localhost:5173
   ```

4. **Accede a la app:**
   - Frontend: [http://localhost:5173](http://localhost:5173)
   - API/Swagger: [http://localhost:5249/swagger](http://localhost:5249/swagger)

## 📝 Configuración requerida

- **Cadena de conexión y SMTP:**
  - Edita `e-commerce-api/appsettings.json` con tu SQL Server y credenciales de email.
- **CORS:**
  - Asegúrate de que `AllowedOrigins` en la API permita la URL de la SPA.
- **URL de la API en la SPA:**
  - Si cambias el puerto de la API, edita la constante `API_URL` en los archivos de servicios de la SPA.
- **Datos de ejemplo:**
  - Usa los comandos SQL en `e-commerce-api/NOTAS.md` para poblar categorías y productos tras migrar la base.

## 📚 Documentación adicional
- Lee los README de cada subcarpeta para detalles específicos de la API y la SPA.
- Consulta `e-commerce-api/NOTAS.md` para tips, comandos SQL y troubleshooting.

## 👨‍💻 Créditos
- Proyecto desarrollado por Acevedo Mario Daniel y Alan Quenardelle (Universidad Tecnológica Nacional UTN)
- Uso académico 