# Desafío SRE/DevOps Engineer Dafiti

Hola candidat@, a continuación te presentamos el siguiente desafio, el cual se compone en tres partes:

1. Habilidades con script y bash linux.
2. Habilidades en kubernetes
3. Proponer una solución cloud de  alta demanda

La idea es que puedas realizar este desafio y posteriormente subirlo a algún respositorio personal como proyecto publico(**gitlab o github**), para así poder revisarlo.

# **1. Habilidades con script y bash linux.**

En la carpeta *bash* encontras la preguntas que se deben responder
Encuentra las preguntas en cada archivo .md ubicado en la carpeta bash.

# **2. Habilidades en kubernetes**

En la carpeta **proyecto-migración** hay un pequeño proyecto que nos interesa empaquetar en Kubernetes. La aplicación tiene
como objetivo registrar actividades en una base de datos de manera escalable. Para evitar
saturar la base de datos y aumentar los tiempos de respuesta, la arquitectura esta
compuesta por:
- Un API que recibe peticiones REST, con los mensajes a registrar.
- Una cola de mensajería.
- Un listener que consume los mensajes desde la cola y los inyecta a una base de datos relacional.
Se espera que los servicios queden escalables y en alta disponibilidad .

Para testear la actual solucion que deseamos migrar, puedes levantarla de la siguiete manera:
ingresar a la carpeta **proyecto-migración** y ejecutar

`docker-compose up `

`curl localhost:8000`

**Que necesitamos en este punto**<p>
Como se menciona en el enunciado dnecesitamos migrar la solución a kubernetes, para ello se necesita lo siguiente:

1. Como ambiente de pruebas se ejecutará en un “minikube”, “mini k8s” o alguna distribución K8S de desarrollo de tu preferencia
2. Detallar en algun readme todos los pasos que permitiran levantar y ejecutar la aplicacion en k8s. EJ: 
   - Descripciond e la solucion y orden de ejecucion de archivos en casos de existir.
   - Requisitos previos para poder levantar la aplicación
   - instrucciones para testear la aplicación.

 # **3. Proponer una solución cloud de  alta demanda**

La idea es exponer una solución para un sitio de alta concurrencia, en la cual este alojada sobre un infraestructura cloud escalable.

Describir mediante un diagrama de solución y explicar que servicios utilizar para la solucion.


