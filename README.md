# Documentacion de docker

- Version instalada de docker
```docker --version```

- Ver la informacion general de docker
```docker info```

## Imagenes

- Imagen
```docker pull [nombre imagen]```
```docker pull mysql:8.0```

- Ver el listado de imagenes
```docker images```

- Eliminar una imagen
```docker rmi [nombre/id]```
```docker rmi mysql```

- Construir una imagen desde un Dockerfile
```docker build -t [imagen] [path]```
```docker build -t mi_imagen .```

## Contenedores

Crear y ejecutar un contenedor
```docker run -d --name [nombre contenedor] -p [ puertos host:contenedor] [nombre imagen]```
```docker run -d --name mi_contenedor -p 3000:80 nginx```

- Listar contenedores en ejecucion
```docker ps```
- Listar contenedores
```docker ps -a```

- Detener contenedor
```docker stop [nombre/id]```
```docker stop mi_contenedor```

- Eliminar un contenedor (detenido)
```docker rm [nombre/id]```

- Eliminar un contenedor (forzar)
```docker rm -f [nombre/id]```

- Iniciar un contenedor 
```docker start [nombre/id]```

- Borra todo lo que no se esta usando (NUKE)
```docker system prune```

# Docker compose
- Levantar servicios definidos en el docker-compose.yml
```docker compose up -d```

- Detener servicios
```docker compose down```