# Repositorio servidor openwebui para integrar con ollama

Configuración de un servidor [openwebui](https://docs.openwebui.com/) en contenedores.

Basado en [How to locally deploy ollama and Open-WebUI with Docker Compose](https://medium.com/@edu.ukulelekim/how-to-locally-deploy-ollama-and-open-webui-with-docker-compose-318f0582e01f)

## Configuracion previa

Si **ollama** esta instalado en otro servidor, considerar las siguientes lineas de código:

```yaml
    environment:
      - 'OLLAMA_BASE_URL=http://192.168.1.62:11434/'
```

## Despliegue

- Antes de ejecutar el despliegue con el archivo docker-compose.yml se debe crear el volumen externo, con el comando:

```bash
docker volume create open-webui-local
```

- Para pruebas de despliegue:

```bash
docker-compose --dry-run up -d
```

- Si esta funcionando correctamente, realizar el despliege respectivo:

```bash
docker-compose up -d
```

### Nota

> [!IMPORTANT]
> 
> No olvidar de agregar los modelos, sino no tendran con que formular las respuestas a las consultas enviadas.

### Referencias:

Repositorio [Git openwebui](https://github.com/open-webui/open-webui)

------

![ArquiTI](./resources/images/guerrero-halcon-round-100.png "ArquiTI") Power by [ArquiTI](https://r0d4nd0-c0n-y4kup3.blogspot.com) in [y4ku-org](https://github.com/y4ku-org)

------
