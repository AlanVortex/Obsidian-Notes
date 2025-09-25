# PWA (Progressive Web Apps)

Las **PWA** son una evolución natural que difumina la barrera entre la web y las aplicaciones.  

---
## ¿Qué NO es una PWA?
- Extensión de navegador  
- Framework  
- Plugin o librería  
- App nativa  
- Responsive design  

---
## ¿Qué SÍ es una PWA?
Una aplicación principalmente desarrollada con un enfoque **Mobile First**, que progresivamente incorpora:
- Push notifications  
- Seguridad (HTTPS)  
- Ligereza y rapidez de carga  
- Actualizaciones constantes (controladas por el desarrollador)  
- Modo offline  
- Acceso a características nativas del dispositivo (GPS, cámara, micrófono, etc.)  

---
## ¿Por qué construir una PWA?
- **Experiencia de usuario mejorada**: se comporta como una app nativa, pero sin necesidad de instalación desde una tienda.  
- **Multiplataforma**: funciona en cualquier dispositivo con navegador moderno, reduciendo costos de desarrollo.  
- **Instalación sencilla**: el usuario puede agregarla al inicio de su dispositivo con un solo clic.  
- **Rendimiento optimizado**: aprovecha *service workers* y caché inteligente para cargar rápido incluso con conexión lenta o sin internet.  
- **Mayor engagement**: gracias a notificaciones push y uso en segundo plano.  
- **SEO y descubrimiento**: al ser una web, es indexable por buscadores, aumentando la visibilidad.  
- **Mantenimiento centralizado**: se actualiza automáticamente al estar en la web, sin depender de procesos de aprobación en tiendas de apps.  
- **Reducción de costos**: no se requiere desarrollar múltiples versiones (iOS, Android, Web), basta con una base común.  

---
## El corazón de una PWA

Los componentes principales que conforman el núcleo de una **Progressive Web App** son:
### Service Worker
- Archivo **JavaScript** con funciones elementales.  
- Controla la caché, las solicitudes de red y el funcionamiento **offline**.  
- Permite mejorar el rendimiento y la experiencia del usuario.  
### Manifest
- Archivo **JSON** que indica cómo se verá la app en la pantalla de inicio (**homescreen**).  
- Define íconos, nombre, colores y comportamiento de la PWA cuando se instala.  
### IndexedDB
- Base de datos local en el navegador.  
- Permite **almacenar información de forma local** para que la aplicación funcione incluso sin conexión.  
### Push Server
- Servicio encargado de **enviar notificaciones push** a los usuarios.  
- Mejora el engagement y permite comunicación directa en tiempo real.  

---
# Conceptos básicos de una PWA

## Requisitos
- Nuestras aplicaciones deben estar disponibles en **HTTPS** (excepto en `localhost`).  
- Esto garantiza seguridad en la comunicación, requisito indispensable para habilitar características como *service workers* y *push notifications*.  

---
## Ciclo de vida de un Service Worker (5 estados)

### 1. Instalando
- El usuario abre la página, se descarga el **HTML**, el **JS** y se registra el **service worker**.  
- Si la instalación es exitosa, pasa al siguiente estado.  
### 2. Instalado (Waiting)
- Si **no existe un service worker previo**, se instala automáticamente.  
- Si ya hay uno en ejecución, el nuevo **espera (waiting)** a que todas las pestañas de la app se cierren.  
- Solo entonces podrá activarse.  
### 3. Activación
- Fase intermedia antes de tomar el control total.  
- Aquí se pueden realizar **actualizaciones del caché** y limpieza de recursos antiguos.  
- El desarrollador controla cuándo actualizar la PWA, para garantizar que los recursos estén listos **offline** antes de usarse en la web.  
### 4. Activado
- El service worker ya tiene el control completo de la aplicación.  
- Se encarga de interceptar peticiones, responder con caché, manejar sincronización en segundo plano y habilitar notificaciones push.  
- A partir de aquí, la PWA puede comportarse como una **app nativa**, incluso sin conexión.  
### 5. Ocioso
- Cuando un nuevo service worker es instalado y activado, el anterior pasa a estado **ocioso**.  
- Permanece en segundo plano hasta que es eliminado completamente.  
- Cada actualización “mata” al anterior y lo reemplaza por el nuevo, asegurando que siempre se ejecute la última versión.  

---
## ¿Cómo ver un Service Worker?

Un **service worker** funciona como un **proxy entre la aplicación y la red**:
- Intercepta los **eventos** (como `fetch`, `push`, `sync`).  
- Decide si responder con datos de la caché o hacer una nueva petición a la red.  
- Detecta cambios en el estado de la aplicación y puede ejecutar lógica en segundo plano.  
- En Chrome DevTools → *Application* → *Service Workers*, se puede inspeccionar su estado, registros y caché.  
