# GITFLOW

Modelo alternativo creación de ramas para proyectos programados (Scrum).

* Para iniciar proyecto con gitflow
`git-flow init

## Ramas Principales ( Se crean solas desde el git-flow init)

* Master : Versión estable del código.
* Develop : Integración continua y desarrollo

# Ramas Auxiliares ( Se pueden crear desde git-flow init)

* Feature : Desarrollo de nuevas características.
* Release : Preparar nueva version para lanzamiento.
* Hotfix : Corrección errores críticos en la “master”.

## Pasos generales

1- Cada vez que se trabaje en una nueva característica, se crea rama “feature” a partir de la “develop” : `git flow feature start <nombre-de-caracteristica>`. 

2- Fusiona la rama “feature” con la “develop”, y elimina la rama “feature”  y cambia a “develop” : `git flow feature finish <nombre-de-caracteristica>`.

3- Crear rama “release” , cuando se haya revisado código, para su lanzamiento : `git flow release start <numero-version>`.

4- Finaliza la rama y la fusiona con la rama “master”, etiqueta el lanzamiento con el numero de versión, y cambia a “develop”. `git flow release finish <numero-version>`.

5- Crear rama “hotfix”, si se descubre un error critico en la rama “master”, se crea “hotfix” para corregir error y lanzar nueva versión,  a partir de la rama “master”, el numero de la versión debe ser el actual: `git flow hotfix start <numero-version>`.

6- Fusiona con la rama “master”, etiqueta la versión corregida con el numero de versión y cambia a “develop” : `git flow hotfix finish <numero-version>`.

## Pasos auxiliares

1- “Bugfix” : Corregir errores críticos en la rama “master” o en una rama de version. Se crea a partir de la rama afectada y se fusiona después : `git flow bugfix start <nombre-erorr>` y `git flow bugfix finish <nombre-error>`.

2- “Support” : Soporte a versiones antiguas de una app que aun se utiliza en producción. Se crea a partir de la “master” y se fusiona después de su corrección : `git flow support star <numero-version>` y `git flow support finish <numero-version>`.