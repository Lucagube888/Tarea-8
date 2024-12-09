<h2>Proyecto: Configuración de Apache con Docker y Múltiples Dominios</h2>

Este proyecto tiene como objetivo configurar un servidor Apache en contenedores Docker, utilizando docker-compose para gestionar los contenedores y asignar direcciones IP fijas. Además, se configurará un DNS interno que resolverá dos dominios hacia la IP del contenedor de Apache, utilizando virtual hosts en el puerto 80 para gestionar cada dominio de manera separada.
Pasos a seguir
1. Preparar el entorno de Docker

    Si no lo tienes configurado, instala Docker y Docker Compose.
    Crea un proyecto inicial que incluya un contenedor con Apache.

2. Configurar un archivo docker-compose.yml

Define al menos dos servicios:

        Apache: el servidor web donde configuraremos los virtual hosts.
        DNS: un servidor DNS interno que resolverá los dominios requeridos.
        
Asigna direcciones IP fija
En el docker-compose.yml del repositorio.
Para que el DNS resuelva los dominios es muy facil, hay que primero de todo hay que entrar en el archivo resolved.conf.
Se encuentra en la ruta /etc/systemd/resolved.conf hay que bajar y descomentarla parte de DNS, poner la ip de tu DNS del .yml poner la tecla numeral y el puerto que estas usando, eso servira para que tu DNS tambien solucione algunas consultas.
Ahora hay que hacer el archivo de las zonas, esta en la carpeta llamada zonas, si esta hecho correctamente al buscar como lo has puesto en el archivozonas te aparecera en google los archivos html que has puesto.
