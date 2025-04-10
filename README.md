# Load Balancer VS Reverse Proxy VS API Gateway

Hablaremos: **Load Balancer**, **Reverse Proxy** y **API Gateway**.

---


## ⚖️ Load Balancer

### Qué es
Distribuye el tráfico entre múltiples instancias de backend para optimizar carga y disponibilidad.

### Tipos
- **L4 (Transport Layer):** TCP/UDP
- **L7 (Application Layer):** HTTP/HTTPS (rutas, headers)

### Características
- Balanceo de carga eficiente
- Alta disponibilidad
- Escalabilidad

### Ejemplos
- HAProxy
- AWS ELB
- Nginx
- Traefik

---

## 🔁 Reverse Proxy

### Qué es
Servidor que recibe peticiones del cliente y las redirige a un backend. El cliente no conoce al servidor real.

### Características
- Oculta servidores internos
- Maneja SSL/TLS
- Caching, compresión
- Seguridad básica (rate limiting)

### Ejemplos
- Nginx
- Apache HTTP Server
- Traefik

---

## 🚪 API Gateway

### Qué es
Punto de entrada centralizado para microservicios. Maneja autenticación, transformación y control de tráfico.

### Características
- Autenticación/autorización
- Rate limiting, logging, tracing
- Transformación de requests/responses
- Agregación de APIs

### Ejemplos
- Kong
- Spring Cloud Gateway
- AWS API Gateway
- Apigee
- Zuul

---

## 📊 Comparación

| Característica         | Reverse Proxy | Load Balancer | API Gateway        |
|------------------------|---------------|---------------|--------------------|
| Enrutamiento           | ✅             | ✅             | ✅                  |
| Balanceo de carga      | ⚠️ (básico)     | ✅             | ⚠️ (a través de otros) |
| Seguridad (SSL, etc.)  | ✅             | ✅             | ✅                  |
| Autenticación/Authz    | ❌             | ❌             | ✅                  |
| Transformación         | ❌             | ❌             | ✅                  |
| Caching                | ✅             | ❌             | ✅ (opcional)       |

---

## 🧭 Cuándo usar cada uno

- **Reverse Proxy:** Para ocultar y proteger tus servidores, manejar SSL o redirigir tráfico.
- **Load Balancer:** Cuando necesitas distribuir carga entre múltiples instancias.
- **API Gateway:** Ideal para microservicios que requieren autenticación, monitoreo y transformación de datos.

