# Proyecto migrations
En el presente documento se indicara como desplegar el proyecto y levantar el minikube
1 - Levantar el cluster en docker:
    `minikube start --driver=docker`
2 - Construir la imagen api:
    `cd api`
    `docker build -t api .`


3 - Construir la imagen listener:
    `cd api`
    `docker build -t listener .`


(En caso de que ocurra un error usar `eval $(minikube docker-env)` y volver a hacer build de las imagenes previas)


4 - Configurar el recurso en el minikube:
    `cd proyecto-migracion`
    `kubectl apply -f api-claim0-persistentvolumeclaim.yaml, listener-claim0-persistentvolumeclaim.yaml, rabbitmq-deployment.yaml, rabbitmq-service.yaml, db-deployment.yaml, db-service.yaml, listener-deployment.yaml, api-deployment.yaml, api-service.yaml`


5 - Validar que los deployments esten en `Runing`:
    `kubectl get pods`


     NAME                       READY   STATUS    RESTARTS   
    |-------------------------|--------|---------|--------|
    |api-8f54d798f-drzds      |  1/1  |Running  |   0    |      
    |db-78b557bbc4-xjsfn      |  1/1  |Running  |   0    |      
    |listener-f76884794-5psx8 |  1/1  |Running  |   0    |      
    |rabbitmq-bb6d77dd6-n6wvf |  1/1  |Running  |   0    |      

6 - Validar los servicios:
    `kubectl get svc`


    NAME         TYPE        CLUSTER-IP         EXTERNAL-IP   PORT(S)    
    |------------|-----------|-----------------|-------------|-------------|
    |api         | ClusterIP |***autoasigned***|    <none>   |     8000/TCP|  
    |db          | ClusterIP |***autoasigned***|    <none>   |     5432/TCP|     
    |rabbitmq    | ClusterIP |***autoasigned***|    <none>   |     5672/TCP|

7 - acceder a la aplicacion
    `minikube service api`

     NAMESPACE | NAME | TARGET PORT |          URL           |
    |-----------|------|-------------|------------------------|
    | default   | api  |             |  ***autoasigned***     |
    
y realizamos el test a la URL asignada por el tunel para el servicio api:

`cur URL`

***response***:
{"message":"Hello World!"}