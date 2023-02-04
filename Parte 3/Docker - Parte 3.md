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