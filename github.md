# GitHub

Es una plataforma de desarrollo colaborativo de software para alojar proyectos.
Sistema de versionamiento ```remoto```.

-----------

## Conceptos

```Push:``` Tomar el repositorio o los cambios pendiente en servidor local y los sube al servidor remoto.

    git push -u origin master

* -u : Nos ayuda a que la proxima vez que queramos hacer push, no necesitemos especificar la rama.
* origin : Nombre del repositorio.
* master : Rama que deseamos enviar.

| Comandos | Descripcion |
| :--- | :--- |
| git push --tags | Toma los tags del repositorio de Git y los sube a GitHub. |
|||


```Pull:``` Toma el repositorio o los cambios pendientes en el servidor remoto y los baja a el servidor local.

```Remote:``` Es la conexion del servidor local al servidor remoto.

    git remote add origin https://github.com/steve/repositorio.git

* add : Nuevo remote.
* origin : El nombre de nuestro remoto.
* https://github.com/steve/repositorio.git : Direccion de GitHub.

```Origin``` es un estandar para referirnos al origen.
Un repositorio local puede tener conexion a varios remotor y la forma de verlos es con el siguiente comando:

    git remote -v

---

## Guia oficial de Gitosis

[¿Qué es Gitosis?](https://wiki.archlinux.org/title/gitosis#:~:text=Gitosis%20is%20a%20tool%20which,system%20accounts%20on%20the%20server.)

[Instalación y configuración](https://github.com/res0nat0r/gitosis)

Guardar su contraseña de GitHub en la máquina **WINDOWS**

[Guardar usuario y contraseña de GitHub](https://docs.github.com/es/get-started/getting-started-with-git/caching-your-github-credentials-in-git#platform-windows)

Guardar su usuario y contraseña en la máquina **LINUX**

[Guardar usuario y contraseña de GitHub en la maquína](https://docs.github.com/es/get-started/getting-started-with-git/caching-your-github-credentials-in-git#platform-linux)

Para usuario de OSx 10.0 o superior, el KeyChain se los maneja automáticamente.

---





