# animeDocker
Setup de docker-compose para descargar anime con Sonarr, Jackett y qbitTorrent.

## Pre-requisitos

Disponer de docker instalado. https://docs.docker.com/get-docker/

## Instalación

Clonar el repositorio en la carpeta donde queramos que se guarden los archivos, se puede editar el fichero de configuración docker-compose.yml para cambiar cada una de las rutas usadas.
```bash
git clone https://github.com/RCRoger/animeDocker.git
```

Ejecutar el siguiente comando:
```bash
cd animeDocker
docker-compose up -d
```

Todo instalado :)

## Funcionamiento

Existen diferentes aplicaciones que se juntan para el funcionamiento del servico:

### Sonarr

Sonarr se encarga de almacenar las series que queramos descargar, descargarlas y relocalizar cada episodio en un directorio ordenado por Serie/Temporada.
Se puede acceder por defecto desde este [link](http://localhost:8989)

Para más información visitad la [documentación oficial de sonarr](https://wiki.servarr.com/sonarr).

### Jackett

Jackett se encarga de ser un proxy entre las llamadas de Sonarr y los diferentes indexers (sitios web de torrents).
Se puede acceder por defecto desde este [link](http://localhost:8989)

Para más información visitad la [documentación oficial de jackett](https://github.com/Jackett/Jackett).

### qBitTorrent

qBitTorrent se encarga de la descarga de los torrents.
Se puede acceder por defecto desde este [link](http://localhost:8080), las credenciales por defecto son:
username:admin
password:adminadmin

Para más información visitad la [documentación oficial de qBitTorrent](https://github.com/qbittorrent/qBittorrent/wiki).

### Jellyfin

Jellyfin se encarga de la reproducción del contenido multimedia.
Se puede acceder por defecto desde este [link](http://localhost:8096), las credenciales por defecto son:
username:admin

Para más información visitad la [documentación oficial de jellyfin](https://jellyfin.org/docs/).

