# Service MQTT Broker

**Autor**: Agustin Bassi - 2021

## Tabla de contenido

* [Introducción](#introducción)
* [Detalles principales](#detalles-principales)
* [Instalar dependencias](#instalar-dependencias)
* [Descargar el código](#descargar-el-código)
* [Ejecutar la aplicación](#ejecutar-la-aplicación)
* [Colaborar](#colaborar)
* [Licencia](#licencia)

## Introducción

MQTT es un protocolo de red de publicación-suscripción, abierto y liviano, que transporta mensajes entre clientes. El protocolo se ejecuta sobre TCP/IP y está diseñado para conexiones con dispositivos y ancho de banda limitados.

Un broker MQTT es un servicio que recibe los mensajes y los enruta a los clientes de destino adecuados. Un cliente MQTT es cualquier dispositivo (desde un microcontrolador hasta un servidor completo) que ejecuta una biblioteca MQTT y se conecta a un broker a través de una red.

Para este proyecto, el broker implementado es `Mosquitto` y se ejecuta sobre `Docker`, de manera que pueda correr de igual manera en diversas plataformas.

## Detalles principales

El archivo `docker-compose.yml` administra los parámetros de ejecución del broker. 

Si querés modificar algún parámetro de configuración del broker podés hacerlo desde el archivo `config/mosquitto.conf`. En caso que quieras que los clientes se conecten al broker con usuario y contraseña descomentá la línea `password_file /etc/mosquitto/pass.txt` y agregá la contraseña de conexión dentro del archivo `auth/pass.txt`.

## Instalar dependencias

Para correr este proyecto es necesario que instales `Docker` y `Docker Compose`. 

En [este documento](https://www.gotoiot.com/pages/articles/docker_installation/index.html) publicado en nuestra web están los detalles para instalar Docker y Docker Compose. Si querés instalar ambas herramientas en una Raspberry Pi podés seguir [esta guía](https://devdojo.com/bobbyiliev/how-to-install-docker-and-docker-compose-on-raspberry-pi) que muestra todos los detalles de instalación.

En caso que tengas algún incoveniente o quieras profundizar al respecto, podes leer la documentación oficial de [Docker](https://docs.docker.com/get-docker/) y también la de [Docker Compose](https://docs.docker.com/compose/install/).

## Descargar el código

Para descargar el código, lo más conveniente es que realices un `fork` de este proyecto a tu cuenta personal haciendo click en [este link](https://github.com/gotoiot/service-mqtt-broker/fork). Una vez que ya tengas el fork a tu cuenta, descargalo con este comando (acordate de poner tu usuario en el link):

```
git clone https://github.com/TU_USUARIO/service-mqtt-broker.git
```

> En caso que no tengas una cuenta en Github podes clonar directamente este repo.

## Ejecutar la aplicación

Cuando tengas el código descargado, desde una terminal en la raíz del proyecto ejecuta el comando `docker-compose up` que se va descargar la imagen de Docker del broker y ponerlo en marcha. Una vez que el broker esté corriendo ya podés conectar distintos clientes.

## Colaborar

¿Te gustó el proyecto? Si es así no dudes en apoyarlo con una estrella en Github desde [la home del proyecto](https://github.com/gotoiot/service-mqtt-broker), esto motiva mucho a seguir adelante con el desarrollo de código para la comunidad. Si estás interesado en recibir novedades cuando se hagan actualizaciones, podes suscribirte desde [este link](https://github.com/gotoiot/service-mqtt-broker/subscription).

Si te gustaría aplicar mejoras a este proyecto podes abrir un hilo de discusión en [este link](https://github.com/gotoiot/service-mqtt-broker/issues/new) para conversarlas y luego podrías enviarlas mediante un `pull request`. 

Finalmente podés compartir este proyecto para que más personas puedan utilizarlo y beneficiarse de esta gran comunidad del software libre.

## Licencia

[MIT](https://choosealicense.com/licenses/mit/)

![footer](doc/gotoiot-footer.png)