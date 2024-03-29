Aquí tienes algunos comandos básicos de Git que son fundamentales para comenzar a trabajar con control de versiones en Git:

### Configuración Inicial:
1. **Configurar Nombre de Usuario:**
   ```bash
   git config --global user.name "Tu Nombre"
   ```

2. **Configurar Correo Electrónico:**
   ```bash
   git config --global user.email "tu@email.com"
   ```

### Crear y Clonar Repositorios:
3. **Inicializar un Repositorio Local:**
   ```bash
   git init
   ```

4. **Clonar un Repositorio Existente:**
   ```bash
   git clone url_del_repositorio
   ```

### Trabajar con Cambios:
5. **Ver el Estado del Repositorio:**
   ```bash
   git status
   ```

6. **Agregar Archivos para Seguirlos:**
   ```bash
   git add nombre_archivo
   ```

7. **Agregar Todos los Archivos Modificados:**
   ```bash
   git add .
   ```

8. **Confirmar los Cambios con un Mensaje:**
   ```bash
   git commit -m "Mensaje descriptivo del commit"
   ```

9. **Hacer Commit de Todos los Cambios (Incluyendo Archivos Eliminados):**
   ```bash
   git commit -am "Mensaje del commit"
   ```

### Ramas (Branches):
10. **Crear una Nueva Rama:**
    ```bash
    git branch nombre_rama
    ```

11. **Cambiar a una Rama Existente:**
    ```bash
    git checkout nombre_rama
    ```

12. **Crear una Nueva Rama y Cambiar a Ella:**
    ```bash
    git checkout -b nombre_rama
    ```

13. **Eliminar una Rama Local:**
    ```bash
    git branch -d nombre_rama
    ```

### Sincronización con Repositorio Remoto:
14. **Agregar un Repositorio Remoto:**
    ```bash
    git remote add nombre_remoto url_del_remoto
    ```

15. **Obtener los Cambios del Repositorio Remoto:**
    ```bash
    git pull nombre_remoto nombre_rama
    ```

16. **Enviar los Cambios al Repositorio Remoto:**
    ```bash
    git push nombre_remoto nombre_rama
    ```

### Historial y Ramificaciones:
17. **Ver el Historial de Commits:**
    ```bash
    git log
    ```

18. **Ver el Historial de Commits en una Sola Línea:**
    ```bash
    git log --oneline
    ```

19. **Ver las Ramas Locales y Remotas:**
    ```bash
    git branch -a
    ```

20. **Comparar Ramas o Commits:**
    ```bash
    git diff nombre_rama_1 nombre_rama_2
    ```

### Deshacer Cambios:
21. **Deshacer Cambios en un Archivo no Añadido:**
    ```bash
    git checkout -- nombre_archivo
    ```

22. **Deshacer el Último Commit (Manteniendo los Cambios):**
    ```bash
    git reset --soft HEAD^
    ```

23. **Deshacer el Último Commit (Eliminando los Cambios):**
    ```bash
    git reset --hard HEAD^
    ```

Estos son solo algunos comandos básicos de Git para comenzar. Git es una herramienta poderosa con muchos más comandos y opciones. Es recomendable aprender más a medida que avances en tus proyectos y necesidades específicas. Puedes consultar la documentación oficial de Git o usar `git --help` para obtener más información sobre un comando específico.

Si tienes alguna pregunta o necesitas más detalles sobre algún comando en particular, no dudes en preguntar. ¡Estoy aquí para ayudar!