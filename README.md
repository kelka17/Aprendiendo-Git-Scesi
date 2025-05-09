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
  
## 📝 clase2: como iniciar repositorio en git  
