# Minecraft-Bedrock-SERVER
Para levantar un server de minecraft bedrock en google cloud o algun otro servicio de la nube, usando maquina virtual



## Pasos a realizar una vez estando en la maquina virtual

### Actualizamos el sistema e instalamos Docker y Docker-Compose

Actualizamos el sistema desplegado.

```
sudo apt-get update
```

Luego instalamos docker.

```
sudo apt-get install docker.io --yes
```

Nos ponemos como usuario root.

```
sudo su
```

e instalamos docker-compose.

```
curl -L https://github.com/docker/compose/releases/download/1.28.5/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

Verificamos que todo esté instalado. Si Docker y Docker-compose están instalados, al ejecutar los siguientes comandos, obtendremos un listado de comandos disponibles.

```
docker 
```

```
docker-compose
```

### Clonamos este repositorio, tomando en cuenta que el mundo sera en bedrock y en modo dificil

```
git clone 
```
