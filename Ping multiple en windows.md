Para enviar pings a múltiples destinos en una sola línea en Windows, puedes usar un `for` loop en un archivo batch (.bat). Aquí te muestro cómo hacerlo:

### Paso a paso:

1. Abre el Bloc de notas u otro editor de texto.

2. Escribe el siguiente código:

```batch
@echo off
for %%G in (google.com microsoft.com amazon.com) do (
    ping -n 5 %%G
)
```

En este ejemplo, `google.com`, `microsoft.com` y `amazon.com` son los destinos a los que se enviarán los pings. Puedes modificar esta lista para incluir los destinos que desees.

3. Guarda el archivo con una extensión `.bat`, por ejemplo, `ping_multiple.bat`.

4. Ejecuta el archivo `.bat` haciendo doble clic en él.

Este script enviará 5 pings a cada uno de los destinos mencionados en el `for` loop.

### Explicación del Script:
- `@echo off`: Esto desactiva la impresión de cada comando en el archivo batch mientras se ejecuta, lo que hace que la salida sea más limpia.
  
- El `for` loop recorre cada uno de los elementos dentro de los paréntesis, en este caso, los nombres de los destinos (`google.com`, `microsoft.com`, `amazon.com`).
  
- `ping -n 5 %%G`: Para cada destino (`%%G` es la variable que representa cada elemento del loop), se ejecutará el comando `ping -n 5`, enviando 5 paquetes de ping a ese destino en particular.

Cuando ejecutes este archivo batch, verás cómo envía pings a cada uno de los destinos y te mostrará los resultados para cada uno de ellos en la consola de Windows.

Recuerda que al usar `%%G` en un archivo batch, dentro de un `for` loop, debes duplicar el símbolo de porcentaje (`%%`) en comparación con el uso habitual de una sola vez (`%`) en comandos interactivos de la consola de Windows.