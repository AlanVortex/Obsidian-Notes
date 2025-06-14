## ¿Qué es seguridad?

> *Es el sentido de estar exento de todo ataque, bug y/o vulnerabilidad.*

---

## ¿Para qué sirven los principios de seguridad?

### 🟢 Reducción
- ➕ Vulnerabilidades
- ➕ Brechas
- ➕ Bugs y ataques

### 🔴 Confianza
- ➕ Menos fallas
- ➕ Estabilidad
- ➕ Control de errores

### 🟡 Protección
- ➕ Información
- ➕ Regulaciones
- ➕ Menos filtraciones

### 🟣 Reputación
- ➕ Evitar gastos
- ➕ Evitar demandas
- ➕ Menor impacto

### 🟠 Soporte
- ➕ Código limpio
- ➕ Auditorías fáciles
- ➕ Seguridad incrementada

### 🟢 Cultura
- ➕ Fomentar la seguridad
- ➕ Parches oportunos
- ➕ Seguridad en CI/CD

## ¿Qué son?

## Principios de Seguridad en el Desarrollo

---

### 🔐 Input Validation

- Nunca confíes de los datos que provienen del usuario o de agentes externos.
- Valida longitud, formato, tipo, rango, etc.
- Usa **whitelist** y **blacklist** para tus datos de entrada.

---

### 🛡️ Least Privilege

- El código, usuarios y procesos deben tener **solo los permisos necesarios** para realizar su tarea.
- No ejecutes procesos con permisos de `admin` si no es necesario.
- Aplica esto a **BDs, APIs y servicios**.

---

### ✅ Authentication & Authorization

- Siempre verifica que el usuario tenga permisos para realizar una acción.
- Nunca confíes en el **frontend** para controlar el acceso.
- Usa autenticación robusta.

---

### 🔒 Data Management

- Encripta datos sensibles tanto **en tránsito como en reposo**.
- Usa algoritmos de **hashing** para datos.
- Nunca guardes contraseñas en texto plano.

---

### 🧪 Injection Prevention

- Escapa adecuadamente fragmentos de **código** y **comandos** para evitar ataques.
- Usa **consultas parametrizadas/preparadas** para evitar **SQL injection**.
- Escapa **XML, HTML, comandos de SHELL** para evitar **XSS o Command Injection**.

---

### ⚠️ Exception Control

- NO muestres errores técnicos al usuario final.
- Usa logs seguros sin mostrar datos sensibles.
- Trata de continuar de forma segura o detenerse sin comprometer el sistema.
- Maneja de manera segura **stack traces**, **SQL** y **rutas**.

---

### 🔄 Dependency Improvement

- ¡Mantén tus dependencias al día!
- Usa herramientas como `npm audit`, **OWASP Dependency-Check**, **Snyk**, etc.
- El software desactualizado puede tener **vulnerabilidades conocidas**.

---

### 🛡️ Secured by Default

- La configuración inicial del sistema debe ser la más segura posible.
- Incluye prácticas como:
  - Deshabilitar funciones innecesarias
  - Cerrar puertos por defecto
  - Eliminar servicios y dependencias sin usar
  - Quitar código comentado

---

### 🧪 Testing & Revision

- Realiza pruebas de seguridad a tu sistema.
- Incluye:
  - Testeos de penetración
  - **Fuzzing**
  - Análisis estático y dinámico
- Revisa código con enfoque en la seguridad.

---
