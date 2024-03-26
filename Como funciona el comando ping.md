El comando `ping` en el símbolo del sistema (CMD) es una herramienta de diagnóstico de red que se utiliza para verificar la conectividad entre dos dispositivos en una red IP. Básicamente, lo que hace es enviar paquetes de datos a una dirección IP específica y luego espera a recibir una respuesta de esa dirección. Esto puede ser útil para comprobar si un dispositivo remoto está accesible a través de la red y para determinar la calidad de la conexión.

A continuación te explico cómo funciona y cómo se utiliza el comando `ping` en el CMD:

### Uso básico:
Para usar `ping`, abre el Símbolo del sistema (CMD) en tu sistema operativo y escribe el siguiente comando seguido de la dirección IP o el nombre de dominio al que deseas hacer ping:

```bash
ping [dirección IP o nombre de dominio]
```

Por ejemplo:

```bash
ping google.com
```

### Funcionamiento:
1. **Envío de paquetes**: Cuando ejecutas el comando `ping`, tu computadora enviará una serie de paquetes de datos a la dirección IP o al nombre de dominio que especificaste.

2. **Espera de respuesta**: Luego, tu computadora esperará respuestas de ese destino. Cada paquete enviado lleva un número de identificación, y cuando el paquete alcanza el destino, el dispositivo al que está dirigido responde de vuelta.

3. **Recibiendo respuestas**: Si el dispositivo objetivo recibe el paquete correctamente, responderá de vuelta a tu computadora. Esto incluye información como el tiempo que tardó el paquete en llegar al destino y volver (esto se llama el tiempo de ida y vuelta o RTT).

4. **Estadísticas**: Después de enviar un número predeterminado de paquetes (generalmente cuatro por defecto en la mayoría de los sistemas), `ping` proporcionará estadísticas resumidas. Esto puede incluir el porcentaje de paquetes perdidos, el tiempo mínimo, máximo y promedio de ida y vuelta, entre otros datos.

### Opciones comunes:

- `-t`: Permite enviar ping de manera continua hasta que se detenga explícitamente con `Ctrl+C`.
  ```bash
  ping -t google.com
  ```

- `-n [número]`: Especifica el número de paquetes a enviar.
  ```bash
  ping -n 10 google.com
  ```

- `-l [tamaño]`: Especifica el tamaño del paquete en bytes.
  ```bash
  ping -l 1000 google.com
  ```

### Ejemplo de resultados:
```
Haciendo ping a google.com [172.217.12.14] con 32 bytes de datos:
Respuesta desde 172.217.12.14: bytes=32 tiempo=10ms TTL=118
Respuesta desde 172.217.12.14: bytes=32 tiempo=11ms TTL=118
Respuesta desde 172.217.12.14: bytes=32 tiempo=9ms TTL=118
Respuesta desde 172.217.12.14: bytes=32 tiempo=10ms TTL=118

Estadísticas de ping para 172.217.12.14:
    Paquetes: enviados = 4, recibidos = 4, perdidos = 0 (0% perdidos),
Tiempos aproximados de ida y vuelta en milisegundos:
    Mínimo = 9ms, Máximo = 11ms, Media = 10ms
```

En este ejemplo, se ha enviado un ping a "google.com", y se muestra que todos los 4 paquetes enviados fueron recibidos sin pérdida, con un tiempo mínimo de 9ms, un tiempo máximo de 11ms y un tiempo promedio de 10ms para el viaje de ida y vuelta.

El `ping` es una herramienta básica pero muy útil para diagnosticar problemas de red, comprobar la conectividad y detectar posibles problemas en una red.