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



