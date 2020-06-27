# Minio con Docker Nginx y SSL

Antes de continuar con la instalación es necesario desplegar el repositorio de [Docker Nginx](https://github.com/dd-ven/docker-nginx.git)

## Requisitos

1. [Docker Engine](https://docs.docker.com/engine/install/)
2. [Docker Compose](https://docs.docker.com/compose/install/)

## Instalación

1. Clonar el repositorio:`` git clone https://github.com/dd-ven/docker-nginx-minio.git``
2. Acceder al directorio: ``cd docker-nginx-minio``
3. Crear una copia de ``.env.sample`` como ``.env``: ``cp .env.sample .env``
4. Modicficar las variables en ``.env`` con un editor de texto: ``nano .env``

````
#Variables de acceso

MINIO_ACCESS_KEY=clavedeacceso
MINIO_SECRET_KEY=clavesecreta

#Variables de red para SSL

VIRTUAL_HOST=hostprueba.es
LETSENCRYPT_EMAIL=info@hostprueba.es
````

5. Desplegar con docker compose: ``docker-compose up -d``