# Docker

1. Instala docker en una máquina y configúralo para que se pueda con un usuario sin privilegios.

   ```bash
   apt install ca-certificates curl gnupg lsb-release
   ```

![](assets/image-20230116120937545.png)

```bash
sudo mkdir -p /etc/apt/keyrings
```

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

![](assets/image-20230116121014939.png)

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

![](assets/image-20230116121046584.png)

