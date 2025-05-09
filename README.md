# :clipboard: Curso Git y GitHub Scesi
![Imagen alt](https://github.com/kelka17/Aprendiendo-Git-Scesi/blob/81075377cafffd52d288274017da07261e23195f/pngimg.com%20-%20github_PNG65.png).
## :computer: Clase 1

## 📝 ¿Qué es Git?
![image](https://github.com/user-attachments/assets/7c86b9c3-ad77-485c-a3c3-a9bb87b3d5bd)

Git es un sistema de control de versiones distribuido que permite a múltiples desarrolladores trabajar en un mismo proyecto de manera coordinada y segura. Fue creado por Linus Torvalds (el mismo creador de Linux) en 2005 para gestionar el desarrollo del kernel de Linux.
##  🔹 ¿Para qué sirve?
- Control de versiones: Permite llevar un historial de cambios de los archivos.
- Colaboración: Varios desarrolladores pueden trabajar en paralelo sin sobrescribir el trabajo de otros.
- Seguridad: Los cambios quedan registrados de manera permanente y segura.
- Deshacer errores: Puedes regresar a versiones anteriores si algo sale mal.
- Ramas: Permite experimentar en paralelo sin afectar el código principal.
### :memo: Repositorio
<p>
Un repositorio en Git es un espacio donde se almacena el historial de cambios de un proyecto, junto con su código fuente, archivos y documentación. Este historial permite
</p>
- Registrar cada modificación (commits).
- Volver a versiones anteriores si es necesario.
- Colaborar con otros desarrolladores de forma ordenada.

Un repositorio puede estar:

- Local: Guardado en tu máquina local.
- Remoto: Guardado en un servidor (como GitHub, GitLab o Bitbucket).
⚙️ Configuración inicial de Git
Después de instalar Git, es necesario configurar tu nombre de usuario y correo electrónico. Esto es importante porque aparecerán en los commits que realizas (como una firma digital).

		-git config --global user.name "Gustavo"
  	
		-git config --global user.email "gustavomamani2464@gmail.com"

## :computer: Clase 2
### 📝 Como iniciar un repositorio en git 
## 1️⃣ Ve al Directorio de tu Proyecto
Si no tienes un proyecto aún, créalo:

		-mkdir mi-proyecto
		-cd mi-proyecto

## 2️⃣ Inicializa el Repositorio Localmente
Para inicializar Git en esa carpeta, ejecuta:

		-git init

💡 Esto creará una carpeta oculta llamada .git, donde Git guarda todo el historial de versiones.

## 3️⃣ Añadir Archivos al Área de Preparación (Staging Area)
Para añadir todos los archivos del proyecto:

		-git add .

💡 El punto (.) indica que se añaden todos los archivos. También puedes especificar archivos individuales:

		-git add index.html

## 4️⃣ Crear un Commit (Guardar los Cambios)
Un commit es un punto de guardado de tus cambios:

		-git commit -m "Inicialización del proyecto"

## :pushpin: Comandos:
### :one: git init
El comando git init se utiliza para inicializar un nuevo repositorio de Git en un proyecto. Esto convierte una carpeta normal en un repositorio que Git puede gestionar, permitiendo el control de versiones de los archivos en esa ubicación.

 	-git init

### :two: git clone 
El comando git clone se usa para copiar un repositorio remoto en tu máquina local, es una forma de obtener una copia completa del proyecto, incluyendo el historial de cambios, ramas y etiquetas.
 
 	-git clone <nombre-del-archivo>
  
### 3️⃣: git status
El comando git status permite ver el estado actual del repositorio.
Podrás visualizar:
- Archivos modificados.
- Archivos que están en el área de staging.
- Archivos que no están siendo seguidos por Git.

	     -git status

### :four: git add
El comando git add sirve para añadir archivos al área de preparación, esta área es donde Git guarda los cambios antes de hacer un commit.

 	-git add archivo.txt #añadir un archivo especifico.
    -git add .         #añadir todos los archivos modificados.

### :five: git commit
Guarda los cambios en el historial del repositorio con un mensaje descriptivo.

	-git commit -m"comentario que quieras guardar"

 ### :six: git log
 El comando git log muestra el historial de commits del repositorio.
 	
  	-git log

### :seven: git branch
El comando git branch permite crear, listar y eliminar ramas en un repositorio, las ramas son versiones paralelas del proyecto donde puedes hacer cambios sin afectar la rama principal.

 	-git branch 
## :computer: Clase 3
### Ramas 🌲 ¿Qué son las Ramas en Git?

![image](https://github.com/user-attachments/assets/116ada14-f7ba-4616-b222-32e387b38043)

Una rama (branch) en Git es una línea de desarrollo independiente. Permite trabajar en funcionalidades nuevas, corregir errores o probar ideas sin afectar la rama principal (main o master).
Imagina las ramas como caminos paralelos que se pueden unir en un solo camino más adelante.

## 🔹 Rama Principal (main/master)
Cuando creas un repositorio, Git genera una rama principal llamada main (antes se llamaba master).
Es la versión "oficial" y estable de tu proyecto.

## 🔹 ¿Para qué sirven?
- Trabajar en nuevas funcionalidades sin afectar el proyecto principal.
- Probar ideas experimentales.
- Colaborar con otras personas en diferentes características.
- Corregir errores sin interrumpir el desarrollo.

## 🚀 Comandos Esenciales para Ramas en Git
## 1️⃣ Crear una Rama Nueva

		-git branch nombre-de-la-rama

💡 Esto crea una nueva rama, pero no te cambia a ella.

## 2️⃣ Cambiarte a una Rama Existente

		-git checkout nombre-de-la-rama

o también:

		-git switch nombre-de-la-rama
## 3️⃣ Crear y Cambiar a la Nueva Rama al Mismo Tiempo

		-git checkout -b nombre-de-la-rama

o también:

		-git switch -c nombre-de-la-rama
## 4️⃣ Ver las Ramas Existentes
	
		-git branch

💡 La rama en la que estás actualmente estará marcada con un *.

## 5️⃣ Unir una Rama a otra (Merge)
Si terminaste tu desarrollo en una rama secundaria y quieres integrarlo en main:

Ve a la rama principal:

		-git checkout main

Haz el merge:

		-git merge nombre-de-la-rama
## 6️⃣ Eliminar una Rama
Después de hacer un merge, puedes borrar la rama:

		-git branch -d nombre-de-la-rama

💡 Si aún no la has fusionado y quieres eliminarla de todas formas:

		-git branch -D nombre-de-la-rama
## 7️⃣ Ver el Historial de Ramas
Para visualizar el historial de commits en todas las ramas de forma gráfica:
	
		-git log --oneline --graph --all

## 🎯 Ejemplo de Flujo de Trabajo con Ramas:
- 1️⃣ Estás en main.
- 2️⃣ Creas una nueva rama para una funcionalidad nueva:

		-git checkout -b nueva-funcionalidad
- 3️⃣ Haces tus cambios y los confirmas:

		-git add .
		-git commit -m "Funcionalidad completada"

- 4️⃣ Vuelves a main y haces un merge:

		-git checkout main
		-git merge nueva-funcionalidad

- 5️⃣ Opcional: Eliminar la rama porque ya no es necesaria:

		-git branch -d nueva-funcionalidad
## :hammer: Conflictos en git

Un conflicto en Git sucede cuando Git no puede combinar automáticamente cambios concurrentes de dos ramas. Por ejemplo, si dos desarrolladores modifican la misma línea de un archivo de distinto modo, Git no sabe cuál mantener y genera un conflicto docs.github.com certidevs.com
-  Lo mismo ocurre si alguien borra un archivo en una rama mientras otro lo modifica en la otra
docs.github.com
-  En estos casos Git detiene la operación (merge o rebase) y deja el archivo en conflicto con marcadores especiales.

## 🔥 Cómo Solucionar un Conflicto en Git (Paso a Paso Claro):
## 1️⃣ Detectar el Conflicto
Cuando intentas hacer un merge o un rebase y Git encuentra un conflicto, te muestra un mensaje como este:

		-Auto-merging archivo.txt
		-CONFLICT (content): Merge conflict in archivo.txt
		-Automatic merge failed; fix conflicts and then commit the result.

Para ver los archivos en conflicto:

		-git status
💡 Git listará los archivos como "both modified".

## 2️⃣ Abrir el Archivo en Conflicto
Dentro del archivo en conflicto, Git inserta delimitadores para que identifiques las diferencias:

		-<<<<<<< HEAD
		-// Esto es lo que existe en tu rama actual
		-console.log("Hola desde main");
		-=======
		-console.log("Hola desde nueva-funcionalidad");
		->>>>>>> nueva-funcionalidad
- <<<<<<< HEAD: La versión de la rama actual (en la que estabas al hacer el merge).
- =======: Separador entre ambas versiones.
- >>>>>>> nueva-funcionalidad: La versión que estás intentando fusionar.

## 3️⃣ Editar el Archivo y Resolver el Conflicto
Tienes que decidir qué parte del código quieres conservar:
- Puedes elegir la versión de HEAD.
- Puedes elegir la versión de nueva-funcionalidad.
- O puedes combinar ambas manualmente.

#### Ejemplo:
Si decides unificar ambas versiones, el resultado podría ser:

		-console.log("Hola desde main y nueva-funcionalidad");
- 💡 Elimina los delimitadores (<<<<<<<, =======, >>>>>>>) antes de guardar.

## 4️⃣ Marcar el Archivo como Resuelto
Una vez que has editado y guardado el archivo, indícale a Git que ya está resuelto:

		-git add archivo.txt

## 5️⃣ Finalizar el Proceso
Para completar la fusión, necesitas un commit que registre el cambio:

		-git commit -m "Conflicto resuelto entre main y nueva-funcionalidad"

## 6️⃣ Verificar que Todo Está Correcto
Para comprobar que no quedan conflictos pendientes:

		-git status

Si todo está bien, Git debería decir: "nothing to commit, working tree clean".

## 🔄 Herramientas para Resolver Conflictos Visualmente
Si prefieres un entorno visual para resolver conflictos:
- Visual Studio Code: Muestra los cambios con botones para seleccionar (Accept Current Change, Accept Incoming Change, Accept Both).
- Sourcetree: Permite ver los conflictos en una interfaz gráfica.
- GitKraken: Ideal para manejar ramas y visualizar conflictos.
- P4Merge / Meld: Herramientas específicas para comparar y unir código.

## :computer: Clase 4
## 📌 ¿Qué es GitHub?
GitHub es una plataforma para alojar proyectos utilizando el sistema de control de versiones Git. Permite colaborar, compartir código y gestionar proyectos de software de forma efectiva y organizada.
## 1️⃣ Crear un Repositorio en GitHub
- Ve a GitHub e inicia sesión.
- Haz clic en New Repository.
- Escribe el nombre del repositorio y selecciona Public o Private.
- Marca la opción para crear un README.md si quieres.
- Haz clic en Create repository.

## 2️⃣ Clonar un Repositorio
Para trabajar localmente, debes clonar el repositorio:

		-git clone https://github.com/usuario/nombre-del-repositorio.git

## 3️⃣ Conectar un Repositorio Local a GitHub
Si creaste un repositorio local con git init, puedes conectarlo a GitHub:

		-git remote add origin https://github.com/usuario/nombre-del-repositorio.git
		-git branch -M main
		-git push -u origin main

## 4️⃣ Subir Cambios a GitHub
Después de hacer cambios, debes:
- Añadir al staging:

		-git add .

- Crear un commit:

		-git commit -m "Descripción del cambio"

- Subir al repositorio remoto:

		-git push origin main

## 5️⃣ Crear y Trabajar con Ramas
- Crear una nueva rama:

		-git checkout -b nombre-de-la-rama

- Cambiar de rama:

		-git switch nombre-de-la-rama

- Subir la rama a GitHub:

		-git push origin nombre-de-la-rama

## 6️⃣ Fusionar Ramas (Merge)

- Cambia a la rama principal:

		-git checkout main

- Haz el merge:

		-git merge nombre-de-la-rama

- Elimina la rama si ya no es necesaria:

		-git branch -d nombre-de-la-rama

## 7️⃣ Resolver Conflictos

Si Git detecta un conflicto:

- Abre el archivo afectado y busca los marcadores <<<<<<<, =======, >>>>>>>.
- Edita el archivo para decidir qué cambios conservar.
- Guarda y añade los cambios:

		-git add nombre-del-archivo

- Finaliza el merge:

		-git commit -m "Conflicto resuelto"

## 8️⃣ Actualizar el Repositorio Local

Para traer cambios del repositorio remoto:

		-git pull origin main

## 9️⃣ Clonar, Forkear y Contribuir

- Fork: Crear una copia de un repositorio en tu cuenta.
- Clone: Descargar esa copia para trabajar localmente.
- Pull Request: Solicitar la fusión de tus cambios al proyecto original.

## :computer: Clase 5
## 📚 ¿Qué es Git Flow?
Git Flow es una metodología de trabajo que define una serie de ramas en Git para manejar de forma ordenada el desarrollo de software en equipo. Fue propuesta por Vincent Driessen y proporciona una estructura clara para trabajar con diferentes tipos de cambios, como nuevas funcionalidades, correcciones de errores y lanzamientos de nuevas versiones.

## 🚀 Ramas Principales en Git Flow
Git Flow se basa en dos ramas principales:

- master: La rama principal de producción. Solo contiene versiones estables del código que han sido lanzadas.

- develop: La rama de desarrollo donde se integran todas las características y correcciones de errores antes de ser lanzadas a producción.

## 🚀 Ramas Secundarias en Git Flow
Git Flow también introduce ramas secundarias para organizar las tareas específicas del flujo de trabajo:

- Feature Branches (Ramas de características):

- Estas ramas se crean para trabajar en nuevas funcionalidades.

- Se crean a partir de la rama develop y se fusionan de nuevo en develop una vez completadas.

- Nombrarlas con feature/nombre-de-la-caracteristica es lo más común.

		-git checkout develop
		-git checkout -b feature/nueva-funcionalidad

- Release Branches (Ramas de liberación):

Estas ramas se crean cuando se tiene una versión lista para ser lanzada, pero se necesitan pequeñas correcciones o pruebas.
Se crean a partir de develop y, una vez completadas las correcciones y pruebas, se fusionan en master (producción) y develop.

		-git checkout develop
		-git checkout -b release/1.0

- Hotfix Branches (Ramas de corrección urgente):

- Estas ramas se utilizan para solucionar errores críticos en producción.

- Se crean a partir de master y se fusionan tanto en master como en develop.

## 📈 Flujo de Trabajo en Git Flow
### Desarrollo de nuevas características:
- Se crea una rama feature desde develop.
- Se trabaja en la funcionalidad y, una vez terminada, se fusiona de vuelta en develop.

		-git checkout develop
		-git checkout -b feature/nueva-funcionalidad  # Realizar cambios
		-git commit -am "Agregada nueva funcionalidad"
		-git checkout develop
		-git merge feature/nueva-funcionalidad

### Preparación de una nueva versión:
Cuando se tiene un conjunto de características listas, se crea una rama release desde develop.
En esta rama se pueden realizar ajustes o correcciones menores.

		-git checkout develop
		-git checkout -b release/1.0 # Realizar pruebas o ajustes
		-git commit -am "Corrección de errores menores"
		-git checkout master
		-git merge release/1.0
		-git checkout develop
		-git merge release/1.0

### Corrección urgente en producción:

Si se detecta un error grave en producción, se crea una rama hotfix desde master.
Una vez solucionado el problema, se fusiona tanto en master como en develop.

		-git checkout master
		-git checkout -b hotfix/correccion-urgente  #Solucionar el error
		-git commit -am "Corregido error crítico"
		-git checkout master
		-git merge hotfix/correccion-urgente
		-git checkout develop
		-git merge hotfix/correccion-urgente
## 📦 Cómo Usar Git Flow con Comandos
###Para facilitar el uso de este flujo de trabajo, puedes usar una extensión de Git llamada Git Flow. Aquí te dejo los comandos más comunes:
Inicializar Git Flow en tu repositorio:

		-git flow init

Esto creará las ramas develop y master y configurará las ramas secundarias (feature, release, hotfix).
### Iniciar una nueva rama de características (feature):

		-git flow feature start nombre-de-la-feature

### Finalizar una rama de características (feature):

		-git flow feature finish nombre-de-la-feature

### Iniciar una nueva rama de liberación (release):

		-git flow release start 1.0

### Finalizar una rama de liberación (release):

		-git flow release finish 1.0
### Iniciar una nueva rama de corrección urgente (hotfix):

		-git flow hotfix start nombre-del-hotfix

### Finalizar una rama de corrección urgente (hotfix):

		-git flow hotfix finish nombre-del-hotfix
## 📚 Ventajas de Usar Git Flow
- Organización clara: Cada tipo de trabajo (nueva funcionalidad, corrección, liberación) tiene su propia rama.

- Mejora la colaboración: Los desarrolladores pueden trabajar en diferentes características sin interferir entre sí.

- Gestión eficiente de versiones: El flujo de trabajo asegura que solo el código probado y estable llegue a producción.

- Facilita la gestión de lanzamientos: Puedes preparar versiones sin afectar el desarrollo de nuevas características.

## :computer: Clase 6
### Buenas practicas 
Las buenas prácticas en el desarrollo de software son un conjunto de principios, metodologías y patrones recomendados que los desarrolladores deben seguir para producir un código de alta calidad, fácilmente mantenible y que fomente una colaboración eficiente dentro de un equipo de trabajo.

## 📝 1. Uso Adecuado de Git y GitHub
### 📂 1.1. Estructura de Repositorios
- Organiza bien tu repositorio: Incluye archivos clave como README.md, .gitignore, y una licencia (LICENSE).
- Utiliza un archivo README.md que explique de qué se trata el proyecto, cómo configurarlo, y cómo contribuir.
- Define una rama principal: Usualmente, la rama principal de producción debe ser master o main, y la de desarrollo debe ser develop.
### 🧑‍💻 1.2. Mensajes de Commit Claros
- Escribe mensajes de commit claros y descriptivos: Usa la siguiente convención para los mensajes de commit:
- Tipo de cambio: (feat, fix, docs, style, refactor, test, chore)

		-git commit -m "feat: agregar funcionalidad de búsqueda"
### 🔀 1.3. Uso de Ramas
- Usa ramas para nuevas características (feature/nueva-funcionalidad), correcciones (hotfix/corrección-error) y lanzamientos (release/v1.0).
- Nunca trabajes directamente sobre la rama main o master. Crea ramas específicas para cada tarea.
### 🚀 1.4. Manejo de Pull Requests (PR)
- Haz Pull Requests (PRs) pequeños: Los PRs deben ser fáciles de revisar y no deben ser demasiado grandes.
- Solicita revisiones de código: Asegúrate de que otros miembros del equipo revisen tu código antes de fusionarlo.
### ⚙️ 1.5. Revisiones de Código
- Sigue un proceso de revisión de código: Asegúrate de que el código cumple con los estándares y no introduce errores ni vulnerabilidades.
- Usa herramientas de análisis estático para detectar posibles problemas de calidad de código.

## 🔍 2. Buenas Prácticas de Programación
###🧩 2.1. Escribe Código Claro y Legible
- Usa nombres de variables descriptivos que sean fáciles de entender.
- Escribe funciones y métodos pequeños: Cada función debe realizar una sola tarea y tener un nombre que describa claramente lo que hace.
- Comenta el código cuando sea necesario, pero no abuses de los comentarios. El código debe ser lo suficientemente claro para que, en la mayoría de los casos, no se necesiten explicaciones.

### 📏 2.2. Sigue un Estilo de Código Consistente
- Usa herramientas de formateo automático como Prettier (para JavaScript) o Black (para Python).
- Establece y sigue convenciones de estilo dentro de tu equipo (nombres de funciones, indentación, uso de corchetes, etc.).

		-Convención de nombres: Usa el estilo camelCase para variables y funciones, y PascalCase para clases.

### 🚦 2.3. Maneja Errores y Excepciones de Forma Adecuada
- No ignores los errores: Utiliza bloques try-catch (en el caso de lenguajes como JavaScript) para manejar errores de forma controlada.
- Usa mensajes de error útiles: Asegúrate de que los errores proporcionen información clara sobre qué salió mal.

## 🔧 3. Buenas Prácticas en la Colaboración
### 👫 3.1. Comunicación Eficiente
- Usa Issues y Pull Requests de manera efectiva: No sólo para discutir cambios, sino también para planificar tareas, reportar errores y hacer seguimientos.
- Etiqueta a las personas correctas en los comentarios de las issues o PRs para asegurarte de que los interesados reciban la información.

### 💬 3.2. Revisión y Retroalimentación Constructiva
- Sé respetuoso y constructivo al hacer revisiones de código. Proporciona feedback claro, especificando tanto lo que está bien como lo que podría mejorar.
- Asegúrate de resolver todos los comentarios antes de fusionar el código.

### 📅 3.3. Mantén una Buena Documentación
- Documenta el código y las decisiones de diseño: Si realizaste una decisión importante en la implementación, asegúrate de dejar una pequeña explicación de por qué se tomó esa decisión.
- Actualiza el README.md cuando sea necesario, especialmente si cambian las dependencias, la configuración o el propósito del proyecto.
## 🛠 4. Buenas Prácticas en la Gestión del Proyecto
###📝 4.1. Establece un Plan de Desarrollo
- Usa metodologías ágiles (Scrum, Kanban) para organizar el trabajo en sprints, tareas y prioridades.
- Define objetivos claros y alcanzables para cada iteración o versión del proyecto.

### 📊 4.2. Integración y Despliegue Continuos (CI/CD)
- Automatiza las pruebas: Configura pipelines para que tus tests se ejecuten automáticamente al realizar un commit o PR.
- Automatiza el despliegue: Usa herramientas de integración continua (como GitHub Actions, Jenkins o Travis CI) para desplegar el código a un entorno de pruebas o producción automáticamente.

### 🛡 4.3. Control de Versiones y Versionado Semántico
-Usa versiones semánticas (SemVer) para etiquetar versiones de tu software. Esto incluye un formato como v1.2.0:

-  Major: Cambios incompatibles con versiones anteriores.
-  Minor: Funcionalidades nuevas compatibles con versiones anteriores.
-  Patch: Correcciones de errores compatibles con versiones anteriores.

### 🔐 4.4. Seguridad
- No incluyas información sensible en el código fuente, como contraseñas o claves API. Usa archivos .env o servicios de configuración segura.
- Revisa dependencias regularmente para asegurarte de que no contienen vulnerabilidades.

## 🌍 5. Buenas Prácticas en el Uso de Git y GitHub
### 🌱 5.1. Trabajar con Repositorios Remotos
- Siempre actualiza tu rama local con los últimos cambios desde el repositorio remoto:

		-git pull origin main
- Utiliza las Pull Requests para integrar cambios: Esto facilita las revisiones y mantiene el historial claro.
### 💡 5.2. Establecer Convenciones de Branching
- Usa un flujo de trabajo de ramas adecuado (Git Flow, GitHub Flow, etc.), y respétalo dentro del equipo.
- Nombra tus ramas de manera clara y coherente según el tipo de tarea que estés realizando (ejemplo: feature/nueva-funcionalidad, bugfix/correccion-error).

## :computer: Clase 7 
## ¿En que casos deshacemos un commit?
Deshacer un commit en Git es algo común y puede hacerse en distintas situaciones dependiendo del contexto y del estado de los cambios. Aquí te explico los casos más comunes y cómo deshacer un commit correctamente en cada uno de ellos:

### 1️⃣ Deshacer un Commit Local (No publicado en GitHub)

Caso: Cometiste un error en un commit, pero aún no lo subiste al repositorio remoto (git push).
Solución: Usar git reset para volver al estado anterior.

-		git reset --soft HEAD~1   # Elimina el último commit pero mantiene los cambios en staging.
- --soft: Elimina el commit, pero conserva los cambios en el área de staging (puedes corregirlos y volver a commitear).
- HEAD~1: Significa "un commit atrás". Puedes cambiar el número si quieres retroceder más commits.
### 2️⃣ Deshacer un Commit y los Cambios (No publicado en GitHub)
Caso: Hiciste un commit que está mal y además quieres borrar los cambios realizados.
Solución: Usar --hard para eliminar el commit y sus cambios.

		-git reset --hard HEAD~1   # Elimina el último commit y descarta los cambios.
⚠️ Advertencia: Esta opción borra los cambios del área de trabajo. No podrás recuperarlos a menos que hagas un reflog.

### 3️⃣ Deshacer un Commit ya Publicado (En GitHub)
Caso: El commit ya se ha hecho push al repositorio remoto, pero necesitas deshacerlo.
Solución: Usar git revert, ya que es seguro y crea un nuevo commit que "revierta" los cambios.

		-git revert HEAD   # Crea un nuevo commit que revierte los cambios del último commit.
Esto no borra el historial, simplemente añade un commit inverso que anula los cambios.
Es ideal para entornos colaborativos donde otros ya podrían estar usando ese código.

### 4️⃣ Deshacer Múltiples Commits (No Publicados en GitHub)
Caso: Te diste cuenta de que varios commits seguidos están mal y quieres volver a un estado anterior.
Solución: Usar git reset indicando la cantidad de commits a deshacer.

		-git reset --soft HEAD~3
Esto elimina los últimos 3 commits, pero mantiene los cambios en staging para corregirlos.

### 5️⃣ Deshacer Múltiples Commits Publicados (En GitHub)
Caso: Ya subiste varios commits incorrectos al repositorio remoto.
Solución: Usar múltiples git revert.

		-git revert HEAD~2..HEAD
Esto crea tres nuevos commits que revierten cada uno de los anteriores de forma segura.

### 6️⃣ Deshacer un Commit Específico (No el último)
Caso: El error está en un commit anterior, pero los siguientes están bien.
Solución: Puedes usar el hash del commit para revertirlo.

		-git log
Luego, revertir el commit:

		-git revert <hash-del-commit>
### ❓ ¿Cuándo usar reset y cuándo revert?
- Situación			- Herramienta	- Explicación
- No has hecho push		- git reset	- Es rápido y directo. No afecta a nadie más.
- Ya hiciste push		- git revert	- Es más seguro. No rompe el historial compartido.
- Estás en producción		- git revert	- Evita conflictos en el repositorio remoto.
- El commit es antiguo		- git revert	- Puedes especificar el hash y revertirlo sin afectar otros cambios.

## :computer: Clase 8
### Trucos de Git
### 🔍 1️⃣ Ver el Historial de Commits en un Formato Amigable

		-git log --oneline --graph --decorate --all
Muestra un historial más visual con ramas y un gráfico de las bifurcaciones.

### 🔎 2️⃣ Buscar un Cambio en el Historial

		-git log -S "texto_a_buscar"
Busca un texto específico dentro de los commits para saber en qué commit se hizo un cambio en particular.

### 🌐 3️⃣ Ver los Cambios en Tiempo Real

		-git diff --color-words
Muestra los cambios línea por línea, resaltando solo las palabras modificadas.
### 📝 4️⃣ Guardar Cambios sin Hacer un Commit (Stash)

		-git stash save "Cambios rápidos"
Almacena temporalmente los cambios para que puedas cambiar de rama sin perder nada.
Para recuperar los cambios:

		-git stash pop
### 🚀 5️⃣ Clonar Solo una Rama Específica

		-git clone -b nombre-rama --single-branch https://github.com/usuario/repositorio.git
Esto evita clonar todo el historial de Git, ahorrando tiempo y espacio.

### ✅ 6️⃣ Deshacer un git add antes del Commit

		-git reset HEAD nombre-del-archivo
Si agregaste un archivo por error al área de staging, con este comando lo quitas sin eliminar los cambios.

### 🚀 7️⃣ Renombrar una Rama

		-git branch -m nombre-nuevo
Si quieres renombrar la rama en la que estás actualmente.
### 🔄 8️⃣ Cambiar al Commit Anterior Rápidamente

		-git checkout @^
El símbolo @ es un alias para HEAD, y el ^ indica un commit anterior.

### 🗑️ 9️⃣ Eliminar una Rama Remota

		-git push origin --delete nombre-de-la-rama
Esto elimina la rama del repositorio remoto.

### 🔁 🔟 Recuperar un Archivo Específico de un Commit Anterior

		-git checkout <commit-hash> -- ruta/del/archivo
Trae de vuelta un archivo de un commit antiguo sin afectar el resto del proyecto.

### ⚡ 1️⃣1️⃣ Ver Qué Cambió en un Commit Específico

		-git show <commit-hash>
Te muestra el detalle del cambio, quién lo hizo y cuándo.

### 🔄 1️⃣2️⃣ Borrar el Último Commit Sin Perder los Cambios

		-git reset --soft HEAD~1
El commit se elimina del historial, pero los cambios permanecen en el área de staging.

### 🔥 1️⃣3️⃣ Borrar Todos los Cambios no Comiteados

		-git reset --hard
Restaura el proyecto al último commit, eliminando cualquier cambio no guardado.

### 🚫 1️⃣4️⃣ Ignorar Archivos Locales sin Modificar .gitignore

		-git update-index --assume-unchanged ruta/del/archivo
Perfecto para ignorar archivos de configuración local sin alterar el .gitignore.

### 🎯 1️⃣5️⃣ Comprobar en Qué Ramas Está un Commit

		-git branch --contains <commit-hash>
Útil para saber si un commit se encuentra en alguna rama específica.

### 🔐 1️⃣6️⃣ Verificar el Autor de un Cambio (Blame)

		-git blame nombre-del-archivo
Muestra línea por línea quién hizo cada cambio y en qué commit.

### 🔄 1️⃣7️⃣ Sincronizar un Fork con el Repositorio Original

		-git remote add upstream https://github.com/original/repo.git
		-git fetch upstream
		-git merge upstream/main
### ⚡ 1️⃣8️⃣ Fusionar Solo un Archivo de Otra Rama

		-git checkout otra-rama -- ruta/del/archivo
Trae solo un archivo de otra rama a la rama actual.

### 📌 1️⃣9️⃣ Limpiar Archivos Borrados sin Hacer Commit

		-git clean -f
Elimina archivos no rastreados que quedaron en el proyecto.

### 💡 2️⃣0️⃣ Atajos para Commits y Push en un Solo Comando

		-git commit -am "Mensaje del commit" && git push
El flag -a añade automáticamente los archivos modificados y el -m define el mensaje.

### 🔎 2️⃣1️⃣ Ver el Último Commit Realizado

		-git log -1
Muestra un resumen del último commit, incluyendo el autor, fecha y descripción.

### 🚀 2️⃣2️⃣ Rebobinar a un Estado Específico y Crear una Rama

		-git checkout -b rama-nueva <commit-hash>
Esto te permite partir desde un commit anterior y continuar el desarrollo desde ahí.

### 🔄 2️⃣3️⃣ Fusionar Ramas sin Fast-Forward

		-git merge --no-ff nombre-de-la-rama
Esto mantiene un historial más limpio y organizado en el merge.

### 🕵️ 2️⃣4️⃣ Ver un Log Resumido de los Últimos 5 Commits

		-git log -n 5 --oneline
  
### 🚀 2️⃣5️⃣ Subir Ramas Nuevas sin Especificar origin

		-git push -u origin nombre-de-la-rama
Esto configura la rama para hacer push automáticamente al remoto sin especificar cada vez.

## Trucos de GitHub
### 🔥 1️⃣ Crear un Repositorio desde la Terminal (sin abrir el navegador)
Si ya tienes un repositorio local y quieres crearlo en GitHub sin abrir el navegador, puedes usar el siguiente comando (requiere GitHub CLI):

		-gh repo create nombre-del-repo --public --source=. --push
- --public: Lo crea como público (puedes cambiarlo a --private).

- --source=.: Usa el repositorio actual como origen.

- --push: Realiza el primer push automáticamente.

### 🚀 2️⃣ Navegar por el Código usando atajos del teclado
#### Dentro de un repositorio en GitHub:
- Presiona t: Abre un buscador de archivos.
- Presiona l: Te permite saltar a una línea específica del archivo.
- Presiona w: Activa/desactiva el modo "blame" para ver quién cambió cada línea.

### 🔎 3️⃣ Buscar Código en Todo GitHub
Si quieres buscar un fragmento de código en todos los repositorios públicos:

		-is:public language:Java "public static void main"
- Puedes filtrar por lenguaje, visibilidad, nombre del repo, entre otros.

### 🎯 4️⃣ Crear Issues Rápidamente desde la URL
Si quieres crear un Issue rápidamente sin entrar a la interfaz:

		- https://github.com/usuario/repositorio/issues/new
Puedes incluso prellenar el título y la descripción con parámetros en la URL.

### ⚡ 5️⃣ Editar Archivos Directamente en GitHub
- Navega al archivo que deseas modificar y presiona el ícono ✏️ (Edit this file).

- GitHub crea un fork automáticamente y te permite crear un PR al terminar.

### 🔄 6️⃣ Restablecer un Archivo a una Versión Anterior
En la vista del archivo, puedes presionar History, seleccionar el commit que quieres y luego pulsar View File. Desde ahí, puedes copiar el contenido o restaurarlo.

### 💡 7️⃣ Usar GitHub Gist para Fragmentos de Código
Si quieres compartir un fragmento de código sin crear un repositorio completo, usa:

		-https://gist.github.com/
Es rápido y fácil para compartir y versionar pequeños bloques de código.

### ✨ 8️⃣ Añadir Badges al README.md
Los badges son insignias visuales que indican el estado del proyecto. Ejemplos:

		-![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
		-![Version](https://img.shields.io/badge/version-1.0.0-blue)
		-![License](https://img.shields.io/badge/license-MIT-green)
Puedes obtener más badges en Shields.io.

### 🔄 9️⃣ GitHub Pages: Publica un Sitio Web desde tu Repositorio
Si tienes un repositorio con un proyecto web, puedes publicarlo usando GitHub Pages:

- Ve a Settings → Pages.
- Selecciona la rama (main o gh-pages).
- ¡Listo! Tu página estará disponible en:

		-https://usuario.github.io/nombre-del-repositorio/
### 🚀 🔟 Crear Plantillas de Issues y Pull Requests
Puedes crear plantillas predeterminadas para Issues y PRs en una carpeta llamada .github/ISSUE_TEMPLATE y .github/PULL_REQUEST_TEMPLATE.md.
Esto facilita que otros contribuyan correctamente al proyecto.

### 🔀 1️⃣1️⃣ Revisar un Pull Request con Comandos de GitHub CLI
Si tienes la CLI de GitHub (gh) instalada, puedes revisar PRs rápidamente:

		-gh pr list               # Listar todos los PRs
		-gh pr checkout 12        # Cambiar al PR número 12
		-gh pr review 12 --approve # Aprobar el PR
### 🗂️ 1️⃣2️⃣ Navegar entre Branches desde la Web
En la interfaz de GitHub, puedes presionar la tecla w y un buscador de ramas se abrirá para cambiar de rama sin salir de la página.

### 🔥 1️⃣3️⃣ Ejecutar Workflows Manualmente en GitHub Actions
Si usas GitHub Actions, puedes ejecutar un workflow manualmente:

- Ve a Actions → Selecciona el workflow.

- Haz clic en Run workflow.

- Elige la rama y ¡listo!

### ⚡ 1️⃣4️⃣ Editar un PR desde GitHub Web
Si detectas un error en un PR y tienes permisos, puedes editar el archivo directamente desde GitHub y el cambio se reflejará en el PR automáticamente.

### 🚀 1️⃣5️⃣ Clonar un Repositorio sin el Historial Completo
Si quieres clonar solo el último commit para ahorrar espacio:

		-git clone --depth 1 https://github.com/usuario/repositorio.git
### 🔎 1️⃣6️⃣ Buscar Commits de un Usuario Específico en un Proyecto
Si quieres saber qué commits hizo un usuario en un proyecto:

		-author:usuario
Puedes usar esto en la barra de búsqueda del repositorio.

### 💬 1️⃣7️⃣ Realizar Comentarios en una Línea Específica
En un Pull Request, haz clic en el número de línea y selecciona + para comentar. Es útil para discutir detalles específicos del código.

### ⚙️ 1️⃣8️⃣ Reabrir un Issue Cerrado Automáticamente
Si un Issue se cerró por error o un commit con "Fixes #ID", puedes reabrirlo manualmente en la interfaz o usar:

		-gh issue reopen ID
### 🎯 1️⃣9️⃣ Crear un Branch desde una Issue
GitHub te permite crear un branch directamente desde una Issue con un solo clic. Esto facilita el rastreo de cambios relacionados.

### 🔥 2️⃣0️⃣ Clonar un Branch Específico sin el Historial Completo

		-git clone -b nombre-del-branch --single-branch https://github.com/usuario/repositorio.git
### 💡 2️⃣1️⃣ Sugerencias Directas en un PR
Puedes sugerir cambios en el código con la opción Add suggestion, lo cual permite al autor aceptarlos directamente.

### 📝 2️⃣2️⃣ Editar Commits en un PR (Squash & Merge)
GitHub permite hacer "Squash & Merge" para combinar múltiples commits en un solo cambio antes de fusionar.
