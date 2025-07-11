# 🔐 Configuración de Seguridad - THE BOX API

## ⚠️ Importante: Configuración de Credenciales

Este archivo contiene información sobre cómo configurar de forma segura las credenciales de la aplicación.

### 📝 Configuración Requerida

Antes de ejecutar la aplicación, debes configurar las siguientes credenciales en `appsettings.json`:

#### 1. **Configuración SMTP (Email)**
```json
"SmtpSettings": {
  "Host": "smtp.gmail.com",
  "Port": 587,
  "EnableSsl": true,
  "User": "tu-email@gmail.com",
  "Password": "tu-contraseña-de-aplicación",
  "From": "tu-email@gmail.com"
}
```

#### 2. **Configuración JWT**
```json
"JwtSettings": {
  "SecretKey": "tu-clave-secreta-muy-larga-y-segura",
  "Issuer": "e-commerce-api",
  "Audience": "e-commerce-client",
  "ExpirationHours": 24
}
```

### 🔑 Cómo Obtener Contraseña de Aplicación de Gmail

1. **Habilita la verificación en dos pasos** en tu cuenta de Google
2. Ve a **Configuración de la cuenta de Google**
3. Selecciona **Seguridad**
4. En "Iniciar sesión en Google", selecciona **Contraseñas de aplicación**
5. Genera una nueva contraseña de aplicación para "Correo"
6. Usa esta contraseña en la configuración SMTP

### 🛡️ Seguridad

- ✅ **Nunca subas credenciales reales a Git**
- ✅ **Usa variables de entorno en producción**
- ✅ **Cambia las claves por defecto**
- ✅ **Usa contraseñas de aplicación, no tu contraseña principal**

### 📋 Template de Configuración

Usa `appsettings.template.json` como base para tu configuración:

```bash
cp appsettings.template.json appsettings.json
# Luego edita appsettings.json con tus credenciales reales
```

### 🚀 Variables de Entorno (Recomendado para Producción)

Para mayor seguridad, considera usar variables de entorno:

```bash
# En Windows
set SMTP_USER=tu-email@gmail.com
set SMTP_PASSWORD=tu-app-password

# En Linux/Mac
export SMTP_USER=tu-email@gmail.com
export SMTP_PASSWORD=tu-app-password
```

### 📞 Soporte

Si tienes problemas con la configuración:
1. Verifica que tu cuenta de Gmail tenga verificación en dos pasos habilitada
2. Asegúrate de usar una contraseña de aplicación, no tu contraseña principal
3. Verifica que el puerto 587 esté abierto en tu firewall

---

**⚠️ Recuerda:** Nunca compartas tus credenciales reales en el código fuente. 