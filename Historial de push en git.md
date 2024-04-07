Para ver el historial de `push` en Git, puedes utilizar el comando `git reflog`. Este comando muestra un registro detallado de todas las acciones realizadas en el repositorio local, incluyendo los `push`, `pull`, `commit`, `reset`, entre otros. A continuación, te muestro cómo puedes usarlo para ver el historial de `push`:

1. Abre la terminal o la línea de comandos.

2. Ve al directorio de tu repositorio Git si no estás allí todavía.

3. Ejecuta el siguiente comando:

   ```bash
   git reflog show --all
   ```

   Este comando mostrará el historial detallado de todas las referencias, incluyendo `push`, `pull`, `commit`, etc.

   Si solo quieres ver las acciones relacionadas con los `push`, puedes filtrar los resultados:

   ```bash
   git reflog show origin/master
   ```

   Esto te mostrará las acciones de `push` realizadas en la rama `origin/master`.

4. También puedes utilizar `grep` para buscar específicamente los `push`:

   ```bash
   git reflog show --all | grep "push"
   ```

   Esto mostrará solo las líneas que contienen "push" en el historial.

Recuerda que `git reflog` muestra el historial local, por lo que si realizas `push` en un repositorio remoto desde otro lugar, esos `push` no aparecerán en el historial local a menos que hayas realizado un `fetch` o `pull` para actualizar tu repositorio local.

Además, si necesitas ver el historial de `push` en un repositorio remoto, como GitHub o GitLab, puedes ir al sitio web correspondiente y ver el registro de actividad o los registros de commits para ver quién ha hecho `push` en qué momento y qué cambios se han subido al repositorio remoto.