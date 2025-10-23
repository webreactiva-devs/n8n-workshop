# Taller de n8n: automatiza tu vida en pocos clics

| Web Reactiva Premium - Con 🧡 para la Comunidad Malandriner

## Instalación de n8n

Existen múltiples maneras de instalar n8n en tu ordenador o en un servidor, en la documentación encontrarás pistas: https://docs.n8n.io/hosting/

Te dejo con algunas descubiertas por nuestra comunidad:


### npm

```
npx n8n
```

### Docker

```
docker volume create n8n_data

docker run -it --rm \
 --name n8n \
 -p 5678:5678 \
 -e GENERIC_TIMEZONE="Europe/Madrid" \
 -e TZ="Europe/Madrid" \
 -e N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true \
 -e N8N_RUNNERS_ENABLED=true \
 -v n8n_data:/home/node/.n8n \
 docker.n8n.io/n8nio/n8n
```

### Docker Compose (gracias 🧡 Camilo)

```
services:
  n8n:
    container_name: n8n
    image: docker.n8n.io/n8nio/n8n
    restart: always
    ports:
      - 5678:5678
    environment:
      - N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true
      - N8N_RUNNERS_ENABLED=true
    volumes:
      - /local/volumes/n8n/:/home/node/.n8n
```

### Instalación en 2 clics en DigitalOcean (gracias 🧡 Miguel)

https://www.youtube.com/watch?v=gtGoJujmLo4

(Alex Ávalos también recomienda Elestio https://elest.io/open-source/n8n)

### Instalación en Coolify

https://www.youtube.com/watch?v=wRuSTFeTd2M

https://www.youtube.com/watch?v=3ZFQLSLmOg8


## Checlist durante la sesión

Cosas que hay que ver durante la sesión

- [ ]  Copiar y pegar JSON
- [ ]  Importar plantillas
- [ ]  Crear credenciales
- [ ]  Pinear datos
- [ ]  Ejecución de pasos concretos
- [ ]  Trigger Chat
- [ ]  Trigger Form
- [ ]  Tiempo de ejecución (flechas moviéndose)
- [ ]  Ejecuciones pasadas

## Más cosas...

> Las veremos en el taller, atento a los cambios de este repositorio ;)




| Hecho con 🧡 para la Comunidad Malandriner
