# Docker

1. Vamos a crear dos redes de ese tipo (BRIDGE) con los siguientes datos: 

   Red1 

   ​	· Nombre: red1 

   ​	· Dirección de red: 172.28.0.0 

   ​	· Máscara de red: 255.255.0.0 

   ​	· Gateway: 172.28.0.1 

   Red2 

   ​	· Nombre: red2 

   Es resto de los datos será proporcionados automáticamente por Docker.

```bash
docker network create --driver=bridge --subnet=172.28.0.0/16 --gateway=172.28.0.1 red1
```

![](assets/Captura.JPG)

2. Poner en ejecución un contenedor de la imagen `ubuntu:20.04` que tenga como hostname `host1` , como IP `172.28.0.10` y que esté conectado a la red1. Lo llamaremos `u1` .

   ```bash
   docker run --name u1 --hostname host1 --ip 172.28.0.10 --network red1 ubuntu:20.04
   ```

![](assets/captura2.JPG)