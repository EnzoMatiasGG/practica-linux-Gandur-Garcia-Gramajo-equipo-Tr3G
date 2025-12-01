# Errores Encontrados y Solución de Problemas

Durante el despliegue de los servicios con Docker Compose, encontramos y solucionamos los siguientes errores intencionales:

## 1. Error en la red del servicio Redis
**Problema:**
Al intentar levantar los contenedores, Docker mostró un error indicando que la red `monitoring-network` no existía.
* **Causa:** En el archivo `docker-compose.yml`, el servicio de `redis` estaba configurado para usar una red llamada `monitoring-network`, pero al final del archivo la red estaba declarada simplemente como `monitoring`.
* **Solución:** Corregimos la línea en el servicio de Redis para que use la red correcta (`monitoring`), coincidiendo con el resto de los servicios.

## 2. Error en el volumen de Grafana
**Problema:**
Docker fallaba al crear el contenedor de Grafana indicando que el volumen no estaba definido.
* **Causa:** El servicio `grafana` intentaba montar un volumen llamado `grafana-data`, pero en la sección `volumes:` al final del archivo, el volumen estaba declarado con el nombre `grafana-storage`.
* **Solución:** Modificamos la declaración del volumen al final del archivo para que coincida con lo que pide el servicio (cambiamos `grafana-storage` por `grafana-data`).

## 3. Target "DOWN" en Prometheus (Nginx)
**Problema:**
Al revisar la interfaz de Prometheus en `http://localhost:9090/targets`, el target de `nginx` aparece en estado **DOWN (Rojo)** con un error de conexión.
* **Causa:** En el archivo `prometheus.yml` se configuró a Prometheus para buscar métricas en `nginx:9113`. Sin embargo, la imagen oficial `nginx:alpine` que estamos usando no expone métricas en ese puerto de forma nativa (se requeriría un *exporter* adicional).
* **Conclusión:** Identificamos que este es un comportamiento esperado según lo indicado en la consigna sobre errores de configuración en los targets. El resto de los targets (como el propio Prometheus) funcionan correctamente en estado **UP**.
