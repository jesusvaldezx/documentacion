# Git

Sistema de versionamiento ```local```, en nuestro equipo.

-----------

## Configuracion Git

| Comandos | Descripcion |
| :--- | :--- |
| git -version | Comando para saber que version de git tenemos instalada. |
| git config -global user.name "Steve Rogers" | Establece el usuario con el que voy a trabajar. |
| git config -global user.email "ejemplo@correo.com" | Establece el correo con el que voy a trabajar. |
| git config --global -e | Revisar el archivo de configuracion global. |
| git init | Inicia el repositorio. |
|||

-----------

## Stage

El ```stage``` es el escenario en el cual esta trabajando ```git```. Para que los archivos sean considerados listos para trabajar, estos deben de ser agregados al stage.

| Comandos | Descripcion |
| :--- | :--- |
| git status | Da informacion de los commits, las ramas y los archivos. |
| git add . | Agrega todos los archivos al stage para darles seguimiento previo a un commit. |
| git reset . | Quita todos los archivos del stage. |
| git add *.html | Agrega todos los archivos html al stage. |
| git status --short | Un resumen de lo ultimo agregado al stage. |


-----------

## Commits

Cuando se ejecuta un ```commit```, se realiza un respal del estado actual de la aplicacion. Considerando todos archivos que estan incluidos en el ```stage```.

| Comandos | Descripcion |
| :--- | :--- |
| git commit -m "Titulo del commit" | Crea un commit nuevo. |
| git checkout --. | Reconstruye el proyecto a como estaba en el ultimo commit. |
| git log | Muestra el historial de commits. |
| git commit --amend -m "Mensaje del commit" | Actualiza el mensaje del ultimo commit. |
|||

-----------

## Ramas

Cada rama nueva que se cree, debe tener como buena practica, el prefico al comienzo de ```rama```, ejemplo ```rama-navbar```.

## Tipos de uniones de ramas
* ```Fast-forward``` Une dos ramas si no hay ningun inconveniente.
* ```recursive``` Analiza los cambios tipo bifurcaciones y los une si no hay problemas.

| Comandos | Descripcion |
| :--- | :--- |
| git config --global init.defaulbranch main | Le da el nombre de "main" a la rama global de los repositorios que se creen. |
| git branch -m master main | Cambia el nombre de la rama "master" a "main". |
| git branch | Nos dice en que rama estamos trabajando. |
| git branch nombreRama | Crea una nueva rama. |
| git branch -b nombreRama | Crea una nueva rama y se mueve hacia ella. |
| git checkout nombreRama | Se mueve hacia otra rama. |
| git merge nombreRama | Une dos ramas. |
| git branch -d nombreRama | Elimina una rama cuando ya no hay riesgo de perder algo. |
| git branch -d nombreRama -f | Borra de manera forzada una rama. |
|||

-----------

## Tags - Etiquetas
* Marcan puntos importantes en nuestra aplicacion(Versiones).
* Son una referenciaa a un commit especifico en el tiempo.
* Mediante los tags podemos crear las versiones o release de los ejecutables.

## Guia para numeros de versiones
Ejemplo: ```v1.0.2```
* ```v1``` (Version Mayor) El primer numero es para cuando hay cambios importantes en la aplicacion, pueden haber cambios que rompan el codigo anterior (Breaking changes).
* ```.0``` Se concidera para cuando se le agrega cierta funcionalidad a la aplicacion.
* ```.2``` (Bug fix) Correcciones de errores 
* Ademas del numero de la version se pueden agregar mas cosas como ```Alpha 1```.

| Comandos | Descripcion |
| :--- | :--- |
| git tag nombreTag | Crea un tag. |
| git tag -d nombreTag | Elimina un tag. |
| git tag -a v1.0.0 -m "Mensaje" | Crea un tag para realizar un release. |
| git tag -a v1.0.0 numeroHash -m "Mensaje" | Crea un tag en un Hash en especifico. |
| git show v0.1.0 | Muestra detalles del commit del tag con esa version. |
|||

-----------

## Stash
Es una especie de rama, en la cual almacenamos cambios de manera temporal, para protejerlos en lo que agregamos otros cambios.

Si se obtiene una lista de ```stash``` como la siguiente:
    
    stash@{0}: WIP on master: c6236b1 Conflictos en Stash resueltos
    stash@{1}: WIP on master: c6236b1 Conflictos en Stash resueltos
    stash@{2}: WIP on master: c6236b1 Conflictos en Stash resueltos

El ```stash``` con el index 0, es el ultimo que se ha agregado.

[Enlace para ver la documentacion oficial de los stash.](https://git-scm.com/docs/git-stash)

| Comandos | Descripcion |
| :--- | :--- |
| git stash | Realiza una especie de commit donde guarda el estado actual de los cambios para posteriormente trabajar con ellos. |
| git stash pop | Toma el ultimo stash y coloca esos cambios y mantendra los cambios que hicimos anteriormente. |
| git stash list | Muestra la lista de stash. |
| git stash clear | Borra todos los stash sin preguntar. |
| git stash apply stash@{2} | Restaura el stash con el index que se le indica. |
| git stash drop stash@{0} | Elimina el stash con el index que se le indica. |
| git stash show stash@{1} | Muestra los cambios del stash con el index que se le indica. |
| git stash save "Mensaje del stash" | Le asigna crea un stash y le asigna un mensaje. |
| git stash list --stat | Muestra una lista de los stash con mas detalles. |
|||

-----------

## Rebase - Rebase Interactivo

- Ordenar commits.
- Corregir mensajes de los commits.
- Unir commits.
- Separar commits.

| Comandos | Descripcion |
| :--- | :--- |
| git rebase master | Actualiza los commits de la rama en la que se esta pocisionado para que sean los ultimos, despues de todos los de la rama master. |
| git rebase -i HEAD~4 | Selecciona los cuatro commit previos al ```HEAD``` para ser editados. |
| git checkout -- README.md | Deshace los cambios hechos solo en el archivo README.md. |
|||


-----------

## Alias

Los alias son abreviaciones que le podemos dar a un comando largo o complejo.

| Comandos | Descripcion |
| :--- | :--- |
| git config --global alias.s "status --short" | Crea un alias, para consultar el status del staga, sustituye ```git status --shhort``` por ```git s```. |
|||

Log

    git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

Status

    git config --global alias.s status --short

Alternativa de Status

    git config --global alias.s status -sb



-----------

## Comandos utiles

| Comandos | Descripcion |
| :--- | :--- |
| git commit -am "Mensaje del commit" | Agrega los archivos al stage y inmediatamente crea el commit. |
| git diff | Ver las diferencias. |
| git diff -staged | Ver los cambios que estan en el stage. |
| git reset --soft HEAD^ | Deshace el ultimo commit y borra los cambios del stage. |
| git reset --mixed HEAD^ | Deshace el ultimo commit y borra los cambios del stage. |
| git reset --hard HEAD^ | Deshace el ultimo commit borrando todo del stage y los archivos. |
| git reflog | Muestra un historial de lo que se ha hecho en el repositorio. |
| git mv NombreUno.md NombreDos.md | Renombra un archivo. |
| git m NombreArchivo | Elimina un archivo pero lo deja en el stage. |
| git reset --hard | Restablece a el ultimo commit. |
|||

-----------

## Notas

* El ```--``` indica que despues viene una palabra completa.
* El ```-``` indica que despues viene abreviaturas.
* El ```.``` indica que se estan tomando en cuenta todos los archivos.
* El ```HEAD``` es el punto donde se encuestra la ultima version de nuestro repositorio.
* El archivo ```.gitkeep``` es para darle seguimiento a un folder aunque este vacio.
* El archivo ```.gitignore``` es para agregar los archivos o directorias que deben de ser ignorados por git.

-----------




