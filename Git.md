# GIT

Software de control de versiones ( Para poder ir a cualquier punto de guardado).

## Git comandos: 

* Para configurar Git
`git config—global user.name”Nombre” ` 
`git config—global user.email”Email” ` 

* Para crear carpeta oculta Git , para poder utilizarlo
`git init`

* Para añadir archivos
`git add .`  Para añadir todos los archivos
`git add “nombre.archivo”` Para añadir un archivo

* Para añadir commit 
`git commit -m “Comentario”`

* Para ver si hay archivos sin subir
`git status`

* Para ver los commit que tengo
`git log`

* Para volver a la version del commit que queramos
`git checkout <hash-commit>`

* Para ver las ramas
`git branch`

* Para crear otra rama
`git switch -c “nombre-rama”`

* Para cambiar de rama
`git switch <nombre-rama>`


# GITHUB

* Para añadir repositorio
`git remote add origin <link-repositorio>`

* Para subir proyecto a repositorio
`git push origin <nombre-rama-que-queremos-subir>`

* Para cambiar de repositorio
`git remote set-url origin <link-nuevo-repositorio>`