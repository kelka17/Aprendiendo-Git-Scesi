# Curso Git y GitHub Scesi
![Imagen alt](https://github.com/kelka17/Aprendiendo-Git-Scesi/blob/81075377cafffd52d288274017da07261e23195f/pngimg.com%20-%20github_PNG65.png).
## Clase 1
### Repositorio
<p>
Un repositorio en Git es un espacio donde se almacena el historial de cambios de un proyecto, junto con su código fuente, archivos y documentación. Este historial permite
</p>
- Registrar cada modificación (commits).
- Volver a versiones anteriores si es necesario.
- Colaborar con otros desarrolladores de forma ordenada.

Un repositorio puede estar:

- Local: Guardado en tu máquina local.
- Remoto: Guardado en un servidor (como GitHub, GitLab o Bitbucket).
## Comandos:
### git init
El comando git init se utiliza para inicializar un nuevo repositorio de Git en un proyecto. Esto convierte una carpeta normal en un repositorio que Git puede gestionar, permitiendo el control de versiones de los archivos en esa ubicación.

 	-git init

### git clone 
El comando git clone se usa para copiar un repositorio remoto en tu máquina local, es una forma de obtener una copia completa del proyecto, incluyendo el historial de cambios, ramas y etiquetas.
 
 	-git clone <nombre-del-archivo>
  
### git status
El comando git status permite ver el estado actual del repositorio.
Podrás visualizar:
- Archivos modificados.
- Archivos que están en el área de staging.
- Archivos que no están siendo seguidos por Git.

 	-git status

### git add
El comando git add sirve para añadir archivos al área de preparación, esta área es donde Git guarda los cambios antes de hacer un commit.

 	-git add <nombre-del-archivo>
