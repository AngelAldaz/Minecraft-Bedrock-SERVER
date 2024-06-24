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

### Activacion del contenedor

Clonamos este repositorio, tomando en cuenta que el mundo sera en bedrock y en modo dificil.

```
git clone https://github.com/AngelAldaz/Minecraft-Bedrock-SERVER.git
```

Una vez clonado entramos a la carpeta creada.

```
cd Minecraft-Bedrock-SERVER
```

Levantamos el contenedor.

```
docker-compose up -d
```

Se identifica el id del contenedor.

```
docker ps
```

Revisamos los logs para comprobar que todo este en orden, no olvides reemplazar *TU_ID_DE_CONTENEDOR* por el id de tu contenedor.

```
docker logs -f TU_ID_DE_CONTENEDOR
```

Debemos de poder observar que el servidor esta corriendo y se encuentra en dificil.

### Agregar cheats a un usuario, si se desea.

Una vez que un usuario ingrese es necesario tomar su "xuid", lo cual es el identificador de cada usuario, para asi poner como administrador si se desea, con el objetivo de permitirle usar cheats, este podremos encontrarlo usando el comando previamente usado para los logs.

Una vez identificado el usuario que se desea usar como administrador es importante cambiar el archivo de 
