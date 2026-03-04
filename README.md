# 📧 Sistema de Correos Masivos v0.0.1

Sistema básico para envío de correos electrónicos masivos con soporte para plantillas. Desarrollado por **Isaac Esteban Haro Torres**.

---

## 📝 Descripción

Sistema profesional de automatización de correo electrónico diseñado para envío masivo de emails personalizados a múltiples destinatarios.

### ¿Qué hace este proyecto?

- **Lectura de contactos**: Importa destinatarios desde archivos CSV/Excel
- **Plantillas dinámicas**: Personaliza emails con variables como nombre, empresa, etc.
- **Envío seguro**: Configuración SMTP con autenticación
- **Logging completo**: Registra todos los envíos con timestamps

---

## ✨ Características Principales

| Característica | Descripción |
|----------------|-------------|
| 📋 **Importación CSV** | Carga contactos desde archivos CSV |
| 📝 **Plantillas HTML** | Crea emails personalizados con Jinja2 |
| 📎 **Adjuntos** | Envía archivos adjuntos múltiple |
| 🔒 **SMTP seguro** | Autenticación SSL/TLS |
| 📊 **Logs detallados** | Historial de envíos realizados |
| ⚙️ **Configuración flexible** | Personaliza remitente, servidor, puerto |

---

## 🛠️ Stack Tecnológico

- **Lenguaje**: Python 3.10+
- **Email**: smtplib, email (stdlib)
- **Templates**: Jinja2
- **Datos**: Pandas
- **DNS**: dnspython (validación de email)
- **Interfaz**: Jupyter Notebook / CLI

---

## 🚀 Instalación y Uso

### Instalación

```bash
pip install pandas jinja2 dnspython
```

### Estructura del archivo de contactos (contactos.csv)

```csv
nombre,email,empresa
Juan Perez,juan@empresa.com,Empresa SA
Maria Garcia,maria@otrafirma.com,Otro Corp
```

### Archivo de plantilla (plantilla.html)

```html
<!DOCTYPE html>
<html>
<body>
    <h1>Hola {{ nombre }}!</h1>
    <p>Te escribo de {{ empresa }} para...</p>
</body>
</html>
```

### Ejecución básica

```python
from correomail import CorreoMasivo

# Configurar SMTP
config = {
    'smtp_server': 'smtp.gmail.com',
    'smtp_port': 587,
    'username': 'tu@email.com',
    'password': 'tu_password'
}

# Inicializar
enviador = CorreoMasivo(config)

# Enviar
enviador.enviar_masivo(
    plantilla='plantilla.html',
    contactos='contactos.csv',
    asunto='Asunto del correo',
    adjuntos=['archivo1.pdf', 'imagen.png']
)
```

---

## 📁 Estructura del Proyecto

```
Correos_Masivos_v0.0.1/
├── correos_masivos_colegios_v0_0_1.ipynb
├── config.py                    # Configuración SMTP
├── plantillas/                  # Plantillas HTML
│   └──bienvenida.html
├── contactos_ejemplo.csv       # Archivo de ejemplo
└── README.md
```

---

## 💡 Casos de Uso

1. **Marketing digital**: Campañas de email marketing
2. **Comunicaciones institucionales**: Notificaciones masivas
3. **Onboarding**: Emails de bienvenida a nuevos usuarios
4. **Alertas automatizadas**: Notificaciones de sistema

---

## ⚠️ Notas Importantes

- Usa App Passwords si usas Gmail
- Evita spam: no envíes demasiados emails en poco tiempo
- Respeta las políticas de cada proveedor de email

---

## 🔧 Configuración SMTP Populares

| Proveedor | Servidor | Puerto |
|-----------|----------|--------|
| Gmail | smtp.gmail.com | 587 |
| Outlook | smtp.office365.com | 587 |
| Yahoo | smtp.mail.yahoo.com | 587 |

---

## 🤝 Contribuciones

¿Agregaste nuevas funcionalidades?
¡Abre un Pull Request!

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
