# 🧩 ¿Qué es GIT?

Git es un sistema de control de versiones distribuido, diseñado para registrar los cambios en archivos y coordinar el trabajo entre varias personas en un proyecto.

---

## 🔧 Clientes populares de Git

- **SurgeForge**  
- **Azure Repos**

---

## 🚗 Diferencia entre `Git` y un `cliente`

En pocas palabras, Git es el **motor** del carro, mientras que un cliente de Git solamente es el **chasis**.

---

## ⚙️ Comandos de `Configuración inicial`

- `git config [scope] [variable] [value]`  
  > Funciona para hacerle configuraciones al repositorio local.  
  > Ejemplo: `git config user.name "CokerAlcocer"`

- `git config --list [scope]`  
  > Enlista todas las configuraciones del repositorio según el alcance.  
  > Ejemplo: `git config --list --local`

---

## 🛠️ Comandos de `Creación y clonación de repos`

- `git init`  
  > Inicia un repositorio dentro de la carpeta donde se ejecute el comando.

- `git clone [url]`  
  > Clona un repositorio a partir de una URL.

# 🔍 Comandos de ‘Estado y seguimiento de archivos’

- `git status`:  
  > Funciona para visualizar los cambios que están *trackeados* y en *staging*.

- `git add [path | . | *]`:  
  > Funciona para *trackear* algún cambio que esté en *stage*.

- `git restore --staged [path | .]`:  
  > Funciona para pasar un cambio *trackeado* al área de *stage* nuevamente.

---

## 💾 Comandos para ‘Guardar cambios (local)’

- `git commit [option] [value]`:  
  > Funciona para guardar los cambios de manera local que se encuentren dentro del *track*.  
  > Ejemplo: `git commit -m “[FIRST_COMMIT] Subida inicial del proyecto”`.

# 🌿 Comandos para ‘Ramas’

- `git branch`:  
  > Funciona para enlistar todas las ramas locales.

- `git branch -a`:  
  > Funciona para enlistar todas las ramas locales y remotas.

- `git branch [name]`:  
  > Funciona para crear una nueva rama.  
  > Ejemplo: `git branch develop`

- `git checkout [branch]`:  
  > Funciona para moverse entre las ramas tanto locales como remotas.

- `git checkout -b [name]`:  
  > Funciona para crear una nueva rama y cambiarse a esa misma.

- `git branch -D [branch]`:  
  > Funciona para eliminar una rama localmente.

- `git merge [branch]`:  
  > Funciona para unir los cambios de la rama en la que se está con otra.  
  > Ejemplo: `git merge develop`

- `git rebase [branch]`:  
  > Funciona para rebasar los cambios de otra rama, es decir, poner mis cambios por encima de los cambios de otra rama.

---

# 🌐 Comandos para ‘Repositorios remotos’

- `git remote add [variable] [url]`:  
  > Funciona para agregar la dirección del repositorio remoto de un proyecto.  
  > Ejemplo: `git remote add origin https://github.com/CokerAlcocer/repo.git`

- `git remote remove [variable]`:  
  > Funciona para eliminar la dirección de un repositorio remoto.  
  > Ejemplo: `git remote remove origin`

- `git fetch`:  
  > Funciona para actualizar el repositorio local en base al remoto.

- `git pull [remote] [branch]`:  
  > Funciona para bajar cambios alojados en el repositorio remoto.

- `git push -u [remote] [branch]`:  
  > Funciona para subir los cambios a una rama del repositorio remoto.  
  > Ejemplo: `git push -u origin main`

---

# 🧪 Comandos para ‘Revisión y comparación’

- `git log`:  
  > Funciona para ver todo el historial de cambios de un repositorio.

- `git diff`:  
  > Muestra las diferencias entre archivos modificados.

- `git show [hash]`:  
  > Muestra los detalles de un commit.

# 💾 Comandos para ‘Almacenar cambios en caché’

- `git stash`:  
  > Funciona para almacenar todos los cambios en caché.

- `git stash list`:  
  > Funciona para enlistar todos los cambios *estasheados*.

- `git stash clear`:  
  > Funciona para eliminar toda la lista de cambios *estasheados*.

- `git stash pop [stash_hash]`:  
  > Funciona para aplicar los cambios dentro del caché y elimina de la lista el mismo.

- `git stash apply [stash_hash]`:  
  > Funciona para aplicar los cambios dentro del caché, pero mantiene el *stash* almacenado.

# ⚠️ Comandos para ‘Deshacer cambios’

- `git reset [path]`:  
  > Funciona para remover un archivo del área de *stage*.

- `git checkout`:  
  > Así a secas, revierte todas las **modificaciones** de la rama, ignorando archivos nuevos.

- `git revert [hash]`:  
  > Funciona para crear un nuevo commit y revierte uno anterior.

- `git reset --hard [hash | HEAD]`:  
  > Funciona para restablecer una rama hasta cierto punto, **deshaciendo** todos los cambios a su paso.

- `git reset --soft [hash | HEAD]`:  
  > Funciona para restablecer una rama hasta cierto punto, **guardando** todos los cambios a su paso en el área de *trackeo*.

