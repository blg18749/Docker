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