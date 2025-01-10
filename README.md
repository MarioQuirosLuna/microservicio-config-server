# CREAR PACKAGE

## Genera el package en target

```bash
$ ./mvnw clean package
```

# EJECUTAR CON DOCKER

## Crear build

```docker
sudo docker build -t config-server:v1 .
```

## Ver imagenes creadas

```docker
sudo docker images
```

## Crear una red para que los contenedores se comuniquen

```docker
sudo docker network create springcloud
```

## Levantar contenedor en puerto externo:virtual / nombre maquina / red / imagen apartir de la que se crea

```docker
sudo docker run -p 8888:8888 --name spring-config --network springcloud config-server:v1
```