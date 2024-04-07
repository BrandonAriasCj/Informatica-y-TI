Para eliminar el último commit en Git, puedes usar el comando `git reset`. Hay diferentes formas de hacerlo dependiendo de lo que quieras lograr: conservar los cambios del commit que estás eliminando, conservar los cambios pero deshacer el commit, o eliminar completamente el commit y los cambios asociados.

### Eliminar el último commit conservando los cambios en el área de trabajo:
```bash
git reset --soft HEAD^
```
- `--soft`: Conserva los cambios en el área de trabajo y en el índice (staging area), pero deshace el commit.

### Eliminar el último commit y los cambios en el área de trabajo:
```bash
git reset --hard HEAD^
```
- `--hard`: Elimina el commit y los cambios en el área de trabajo y el índice.

Ten en cuenta que cuando uses `--hard`, **todos los cambios que estén en el commit que estás eliminando se perderán**. Asegúrate de haber guardado todo lo que necesitas antes de ejecutar este comando.

Después de ejecutar uno de estos comandos, si ya has compartido estos cambios en un repositorio remoto, deberás forzar la actualización del repositorio remoto con `git push origin <branch> --force` para sincronizar el repositorio remoto con tu repositorio local.

Si estás trabajando en un repositorio colaborativo, ten en cuenta que forzar una actualización del repositorio remoto puede causar problemas a otros colaboradores si ya han basado su trabajo en el commit que estás eliminando.

**Importante**: Si has realizado un `git reset --hard` y luego te das cuenta de que cometiste un error al hacerlo, es posible que puedas recuperar el commit perdido utilizando el comando `git reflog` para encontrar el hash del commit y luego haciendo `git reset --hard <commit-hash>`.

Antes de realizar acciones drásticas como eliminar commits, siempre es recomendable hacer una copia de seguridad de tus cambios importantes.