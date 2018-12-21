# Inicializar proyecto 

## 1-Crear imagen 

     docker build -t lts-alpine ./docker

## 2-Crear Contenedor en powerShell or Linux.

      docker run --rm -d -v ${PWD}/docker:/usr/docker -p 80:3000 --name demoapp -i lts-alpine

  
     **Nota: Debido al Firewall de Windows expongo mi localhost:80**

## 3 - Filtros Sobre Procesos Docker 

    docker ps -a -q --filter="name=demoapp" 


## 4- Acceder a contenedor

    docker exec -it -t demoapp /bin/sh

## 5- Instalar dependencias

    npm init 
    npm install express --save 



## 6- Detener  contenedor

    docker stop demoapp

