# Solutions

## Punto 1:
- https://github.com/kerodriguezm/DevopsTestDafiti/tree/dev/bash/archivos.md
- https://github.com/kerodriguezm/DevopsTestDafiti/tree/dev/bash/sistema.md

## Punto 2:
Las intrucciones y la solucion estan dentro del directorio  proyecto-migracion:
- https://github.com/kerodriguezm/DevopsTestDafiti/tree/master/dev/proyecto-migracion

## Punto 3:

***Diagrama:***

![alt text](https://github.com/kerodriguezm/DevopsTestDafiti/blob/dev/diagrams/Diagrama.png)

Los servicios que se proponen son los siguientes:

***API REST:*** Para una comunicacion sincrona, en esta api se creara el recurso con los methodos necesarios para poder procesarlos en la lambda.

***Function Lambda:*** Debido a que el proyecto solo se usara cada vez que se realice una peticion lo mejor seria usar una lambda para que procese las solicitudes a las colas del ActiveMQ, 
no seria presindible un servicio para este tipo de procesos de acuerdo a lo requerido.

***ActiveMQ:*** El servicio de agentes de mensageria, configurar las colas atravez de un xml.

***EKS(Elastic Kubernetes Service):*** Un servicio de kubernetes para que realice el proceso de cargar a la base de datos.

***RDS (Relational Database Service):*** Para operar y escalar una base de datos Postgres, generando instancias de lectura y escritura,
en caso de realizar lecturas muy extensas dicha instancia no interrumpira el flujo de insercion.