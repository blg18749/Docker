# Docker

1.  Crea un volumen docker que se llame `miweb`.

```bash
docker volume create miweb
```

![](assets/captura1.png)

2. Crea un contenedor desde la imagen `php:7.4-apache` donde montes en el directorio `/var/www/html` (que sabemos que es el DocumentRoot del servidor que nos ofrece esa imagen) el volumen docker que has creado.

```bash
docker run -d --name apache1 -v miweb:/var/www/html php:7.4-apache
```

![](assets/captura2.png)

3. Utiliza el comando `docker cp` para copiar un fichero `index.html` en el directorio `/var/www/html`.

```bash
docker cp index.html apache1:/var/www/html
```

![](assets/captura3.png)

4. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html.`

![](assets/captura4.png)

5. Borra el contenedor

   ```bash
   docker stop idcontenedor && docker rm idcontenedor
   ```

   ![](assets/captura5.png)

6. Crea un nuevo contenedor y monta el mismo volumen como en el ejercicio anterior.

   ```bash
   docker run -d --name apache1 -v miweb:/var/www/html php:7.4-apache
   ```

   ![](assets/captura6.png)

7. Accede al contenedor desde el navegador para ver la información ofrecida por el fichero `index.html`. ¿Seguía existiendo ese fichero?

   Si, al usar el mismo volumen.

![](assets/captura7.png)