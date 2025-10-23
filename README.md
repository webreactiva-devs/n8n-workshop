# Taller de n8n: automatiza tu vida en pocos clics

> Web Reactiva Premium - Con 🧡 para la Comunidad Malandriner

<img width="2095" height="900" alt="image" src="https://github.com/user-attachments/assets/44b70b9e-a243-4e38-939c-8aa3ad2d0470" />


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

## Workflows para copiar y pegar

### Agente de IA sencillo

https://github.com/webreactiva-devs/n8n-workshop/blob/main/workflows/Ejemplo%20AI%20Agent%20(Groq).json

¿Qué credenciales necesitas para que funcione?
- Cuenta gratutida de Groq para tener modelos de IA


### Email dirairo de los repos trending de Github

https://github.com/webreactiva-devs/n8n-workshop/blob/main/workflows/GitHub%20Trending%20Top%205%20-%20PROD%20(1-1).json

¿Qué credenciales necesitas para que funcione?
- Cuenta gratutida de Groq para tener modelos de IA

### Bot de Telegram que transcribe notas de voz para guardar o recuperarls de una base de datos

https://github.com/webreactiva-devs/n8n-workshop/blob/main/workflows/Telegram%20Audio%20Notes%20PROD.json

¿Qué necesitas para qué funcione?
- Cuenta en OpenAI Platformrm para la transcripción
- Cuenta de Groq para modelos de IA gratuita
- Un bot de telegram (el token)
- Acceso a una base de datos de Notion con [esta estructura](https://www.notion.so/29514d1a96d181fc8529e22d3126f870?v=29514d1a96d181989117000ce7f74218&source=copy_link)

### RAG para consultar una página sin buscador

https://github.com/webreactiva-devs/n8n-workshop/blob/main/workflows/Sabelotodo%20Claude%20Code%20Awesome%20PROD.json

¿Qué credenciales necesitas para que funcione?
- Cuenta en OpenAI Platform para tener acceso a los embeddings
- Cuenta gratutida de Groq para tener modelos de IA

## Recursos

- https://n8n.io/workflows/
- https://agents.sabrina.dev/
- https://github.com/Zie619/n8n-workflows
- https://www.n8n-mcp.com/


## Checklist durante la sesión

- [x]  Copiar y pegar JSON
- [x]  Importar plantillas
- [x]  Crear credenciales
- [x]  Pinear datos
- [x]  Ejecución de pasos concretos
- [x]  Trigger Chat
- [x]  Trigger Form
- [x]  Tiempo de ejecución (flechas moviéndose)
- [x]  Ejecuciones pasadas
 





> Hecho con 🧡 para la Comunidad Malandriner
