# Notas del Proyecto E-Commerce API + SPA

## 1. API RESTful (ASP.NET Core)
- Estructura profesional: Controllers, Services, Repositories, DTOs, Models, Interfaces.
- Seguridad: JWT, hash+salt, endpoints protegidos.
- Funcionalidad:
  - Registro, login, recuperación de contraseña por email (SMTP).
  - CRUD de productos y categorías, paginación.
  - Generación y validación de códigos QR con expiración.
- Configuración flexible (`appsettings.json`): conexión a base de datos, SMTP, CORS.
- CI/CD: GitHub Actions configurado.
- Documentación: README profesional generado.
- Migraciones limpias y sincronizadas.

## 2. Configuración de Email (SMTP)
- Puedes usar Gmail, Outlook, Yahoo, Zoho, etc.
- Para Gmail, activa 2FA y genera una “contraseña de aplicación”.
- Ejemplo de configuración:
  ```json
  "SmtpSettings": {
    "Host": "smtp.gmail.com",
    "Port": 587,
    "EnableSsl": true,
    "User": "tu-email@gmail.com",
    "Password": "contraseña-de-aplicacion",
    "From": "tu-email@gmail.com"
  }
  ```

## 3. SPA (Single Page Application)
- Recomendado: React + Vite (JavaScript).
- Carpeta separada `/e-commerce-spa` al mismo nivel que la API.
- Abrir la carpeta madre en Cursor para trabajar en ambos proyectos.
- Componentes básicos: Login, Registro, Listado de productos, Recuperación de contraseña.

## 4. Pruebas y despliegue
- Probar la API con Swagger, Postman o la SPA.
- CORS configurado para permitir peticiones desde la SPA.
- Compartir el proyecto asegurando que `appsettings.json` esté bien configurado.

## 5. Exportar y guardar el chat
- Puedes copiar y pegar este archivo en Google Docs, Notion, Word, etc.
- También puedes guardar el chat como PDF desde el navegador.

## 6. Recomendaciones finales
- Nunca compartas contraseñas reales en público.
- Usa cuentas de email dedicadas para pruebas.
- Personaliza el README con capturas o videos si lo requiere la entrega.
- Si tienes dudas sobre la SPA, puedes seguir consultando o pedir ejemplos de código. 

---

## Comandos SQL para poblar la base de datos desde cero

### 1. Insertar categorías

```sql
INSERT INTO Categories (Name, Description) VALUES
('Keyboards', 'Mechanical keyboards and accessories'),
('Mice', 'Gaming and productivity mice'),
('Monitors', 'High refresh rate and 4K monitors');
```

### 2. Insertar productos

```sql
INSERT INTO Products (Name, Description, Price, Stock, ImageUrl, CategoryId) VALUES
('Keychron K6', 'Compact wireless mechanical keyboard with RGB backlight.', 79.99, 10, 'https://cdn.shopify.com/s/files/1/0059/0630/1017/products/K6_RGB_Aluminum_1_800x.png', 1),
('Ducky One 2 Mini', '60% mechanical keyboard, double-shot PBT keycaps, RGB.', 109.99, 8, 'https://www.duckychannel.com.tw/en/Ducky-One-2-Mini/images/One2Mini_1.jpg', 1),
('Logitech G Pro X Superlight', 'Ultra-light wireless gaming mouse.', 129.99, 15, 'https://resource.logitechg.com/w_800,c_limit,q_auto:best,f_auto,dpr_1.0/d_transparent.gif/content/dam/gaming/en/products/pro-x-superlight/gallery/pro-x-superlight-gallery-1.png', 2),
('Dell UltraSharp U2720Q', '27-inch 4K USB-C monitor for professionals.', 499.99, 5, 'https://i.dell.com/sites/csimages/Video_Imagery/all/ultrasharp-u2720q-monitor.png', 3);
```

### 3. Verificar los datos

```sql
SELECT * FROM Categories;
SELECT * FROM Products;
```

> Ejecuta estos comandos en SQL Server Management Studio o Azure Data Studio después de aplicar las migraciones. 