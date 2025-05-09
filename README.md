# :clipboard: Curso Git y GitHub Scesi
![Imagen alt](https://github.com/kelka17/Aprendiendo-Git-Scesi/blob/81075377cafffd52d288274017da07261e23195f/pngimg.com%20-%20github_PNG65.png).
## :computer: Clase 1

## 📝 ¿Qué es Git?
Git es un sistema de control de versiones distribuido que permite a múltiples desarrolladores trabajar en un mismo proyecto de manera coordinada y segura. Fue creado por Linus Torvalds (el mismo creador de Linux) en 2005 para gestionar el desarrollo del kernel de Linux.
##  🔹 ¿Para qué sirve?
- Control de versiones: Permite llevar un historial de cambios de los archivos.
- Colaboración: Varios desarrolladores pueden trabajar en paralelo sin sobrescribir el trabajo de otros.
- Seguridad: Los cambios quedan registrados de manera permanente y segura.
- Deshacer errores: Puedes regresar a versiones anteriores si algo sale mal.

Ramas (Branches): Permite experimentar en paralelo sin afectar el código principal.
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
### 
  
  
