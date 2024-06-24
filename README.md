# Minecraft-Bedrock-SERVER

Guía para levantar un servidor de Minecraft Bedrock en Google Cloud o algún otro servicio en la nube usando una máquina virtual.

## Pasos a seguir en la máquina virtual

### Actualizar el sistema e instalar Docker y Docker-Compose

1. **Actualizar el sistema:**

    ```bash
    sudo apt-get update
    ```

2. **Instalar Docker:**

    ```bash
    sudo apt-get install docker.io --yes
    ```

3. **Convertirse en usuario root:**

    ```bash
    sudo su
    ```

4. **Instalar Docker-Compose:**

    ```bash
    curl -L "https://github.com/docker/compose/releases/download/1.28.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    chmod +x /usr/local/bin/docker-compose
    ```

5. **Verificar las instalaciones:**

    Para Docker:

    ```bash
    docker
    ```

    Para Docker-Compose:

    ```bash
    docker-compose
    ```

### Activación del contenedor

1. **Clonar el repositorio:**

    ```bash
    git clone https://github.com/AngelAldaz/Minecraft-Bedrock-SERVER.git
    ```

2. **Acceder a la carpeta del repositorio clonado:**

    ```bash
    cd Minecraft-Bedrock-SERVER
    ```

3. **Levantar el contenedor:**

    ```bash
    docker-compose up -d
    ```

4. **Identificar el ID del contenedor:**

    ```bash
    docker ps
    ```

5. **Revisar los logs para asegurar que todo esté en orden:**

    Reemplazar `TU_ID_DE_CONTENEDOR` por el ID de tu contenedor.

    ```bash
    docker logs -f TU_ID_DE_CONTENEDOR
    ```

### Agregar permisos de administrador (cheats)

1. **Obtener el "xuid" del usuario:**

    Observa los logs para encontrar el identificador del usuario (xuid).

2. **Modificar el archivo `permissions.json`:**

    Reemplaza `TU_XUID` por el xuid del usuario al que deseas otorgar permisos de administrador.

    ```json
    [
      {
        "permission": "operator",
        "xuid": "TU_XUID"
      }
    ]
    ```

3. **Reiniciar el contenedor:**

    Reemplazar `TU_ID_DE_CONTENEDOR` por el ID de tu contenedor.

    ```bash
    docker restart TU_ID_DE_CONTENEDOR
    ```

4. **Comprobar los logs para verificar que todo esté correcto:**

    ```bash
    docker logs -f TU_ID_DE_CONTENEDOR
    ```

¡Y listo! Ya puedes disfrutar de tu servidor de Minecraft Bedrock.
