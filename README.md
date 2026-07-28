# 🚀 n8n - Plataforma de Automatización de Flujos de Trabajo

n8n es una plataforma de automatización de código abierto que permite conectar aplicaciones, servicios y APIs mediante flujos de trabajo visuales.

---

# 📋 Requisitos

Antes de comenzar, asegúrate de tener instalado alguno de los siguientes:

* **Node.js** (para ejecutar con `npx`)
* **Docker** (para ejecutar mediante contenedores)

---

# ⚡ Inicio Rápido

## Opción 1: Ejecutar con NPX

Si tienes **Node.js** instalado, puedes iniciar n8n con un solo comando:

```bash
npx n8n
```

Una vez iniciado, abre tu navegador y visita:

```
http://localhost:5678
```

---

## Opción 2: Ejecutar con Docker

### Crear un volumen para almacenar los datos

```bash
docker volume create n8n_data
```

### Ejecutar el contenedor

```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v n8n_data:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n
```

Cuando el contenedor esté en ejecución, accede desde tu navegador:

```
http://localhost:5678
```

---

# 📁 Persistencia de Datos

El volumen Docker:

```text
n8n_data
```

permite conservar:

* Credenciales
* Workflows
* Configuración
* Variables de entorno
* Historial de ejecuciones

Aunque el contenedor sea eliminado, la información permanecerá almacenada en este volumen.

---

# ☁️ Credenciales de Google Cloud

Para utilizar servicios como:

* Google Drive
* Gmail
* Google Sheets
* Google Calendar
* Google Docs
* Google Cloud APIs

es necesario crear credenciales desde Google Cloud.

Accede al siguiente enlace:

> https://cloud.google.com/

Desde la consola podrás:

1. Crear un nuevo proyecto.
2. Habilitar las APIs necesarias.
3. Configurar la pantalla de consentimiento OAuth.
4. Crear credenciales OAuth 2.0 o cuentas de servicio, según el caso.
5. Utilizar las credenciales dentro de n8n.

---

# 🌐 Acceso

Una vez que n8n esté en ejecución, abre:

```text
http://localhost:5678
```

Desde allí podrás crear, editar y administrar tus flujos de trabajo.

---

# 📚 Recursos

* Sitio oficial de n8n: https://n8n.io/
* Documentación: https://docs.n8n.io/
* Google Cloud Console: https://cloud.google.com/

---

# ✅ Tecnologías

* n8n
* Docker
* Node.js
* Google Cloud
* OAuth 2.0

---

# 📄 Licencia

Este proyecto utiliza **n8n**, una plataforma de automatización de código abierto. Consulta la documentación oficial para obtener información sobre su licencia y uso.
