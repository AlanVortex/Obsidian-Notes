# 🔄 ¿Qué es un flujo de trabajo?

Son estrategias organizativas que definen cómo los desarrolladores colaboran y gestionan el código en un repositorio.

---

# 🧭 Flujos de trabajo

## 1. 🟣 Centralized Workflow

> Todos los desarrolladores trabajan directamente sobre una única rama principal, normalmente llamada `master` o `main`.

✅ Simple y fácil de entender  
⚠️ Puede generar conflictos si varios desarrollan al mismo tiempo

---

## 2. 🟡 Feature Branch Workflow

> Cada nueva funcionalidad se desarrolla en una rama separada, y luego se fusiona mediante un merge a la rama principal.

✅ Facilita el trabajo paralelo  
✅ Cada cambio es aislado  
⚠️ Requiere mayor gestión de ramas

---

## 3. 🟢 Git Flow

> Usa ramas específicas para desarrollo, producción, nuevas funcionalidades, correcciones y versiones.

🔀 Ramas comunes:
- `main`: rama de producción
- `develop`: rama de desarrollo
- `feature/*`: nuevas funcionalidades
- `release/*`: preparación de versiones
- `hotfix/*`: correcciones urgentes

✅ Ideal para proyectos grandes  
⚠️ Puede ser complejo para proyectos pequeños

---

# 🔄 Flujos de trabajo en Git

Los flujos de trabajo definen cómo los desarrolladores colaboran y organizan los cambios en un proyecto versionado con Git. A continuación, se presentan dos de los workflows más comunes:

---

## 🍴 Forking Workflow

> Cada desarrollador trabaja en una **copia** (fork) del repositorio.  
> Luego, proponen cambios mediante un **Pull Request** hacia el repositorio original.

✅ Ideal para:  
- Proyectos open source  
- Equipos con contribuciones externas  
- Control estricto del repositorio original

---

## 🐙 GitHub Flow

> Basado en la rama `main`, cada cambio se realiza en una **rama separada** y se somete a revisión antes de integrarse.

✅ Ideal para:  
- Desarrollos continuos  
- Equipos que hacen despliegues frecuentes  
- Proyectos con integración continua (CI/CD)

---

## ⚖️ Ventajas y ‘desventajas’ de usar flujos de trabajo en Git

### ✅ Ventajas:

- **Organización del desarrollo**:  
  Permiten separar claramente el trabajo.

- **Colaboración efectiva**:  
  Facilitan que varios desarrolladores trabajen en paralelo.

- **Mejora la calidad del código**:  
  Se reduce el riesgo de errores en producción.

- **Control de versiones y lanzamientos**:  
  Ayuda a tener versiones claras en general.

---

### ❌ Desventajas:

- **Curva de aprendizaje**:  
  Los flujos avanzados pueden ser complejos para equipos nuevos.

- **Mayor carga de gestión**:  
  La necesidad de monitorear los repositorios puede ser tediosa.

- **Riesgo de conflictos**:  
  Pueden existir conflictos al hacer merge si los cambios no coinciden.

- **Puede relentizar el trabajo**:  
  Las revisiones obligatorias, pruebas y esperas para aprobar un PR pueden demorar entregas urgentes.

---

