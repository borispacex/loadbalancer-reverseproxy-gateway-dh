# Reverse proxy


## ⚙️ ¿Qué hace cada componente?

- **Nginx**: Actúa como reverse proxy.
- **App1**: Una mini app que devuelve una página HTML con el mensaje "Hola desde App 1".
- **App2**: Similar a App1 pero con el mensaje "Hola desde App 2".

## 🧪 Cómo probarlo

### 1. Clonar el proyecto (o crear los archivos)

Asegúrate de tener esta estructura de carpetas y archivos.

├── docker-compose.yml 
├── nginx/ 
│ └── default.conf 
├── app1/ 
│ └── index.html 
├── app2/ 
│ └── index.html

### 2. Ejecutar los contenedores

En la raíz del proyecto:

```bash
docker-compose up
```

