# Kubernetes 

Es un sistema opensorce para la automatizar el despligue, escalado y administracion de aplicaciones en contenedores. Tambien conocidos como  k8s (Pronounced Kate's).

Escalabilidad: capacidad de los sistemas para adaptarce al crecimiento por demanda y complejidad. 

- Tipos de Escalabilidad 
  -  Vertical:
      Este tipo de escalabilidad es cuando, en un mismo nodo nostros lé aumentamos su porcesaminto y  memoria. Esta forma no es para las más recomendable cuando la aplicacion esta en crecimiento

  -  Horizonal:
     Este tipo de escalabilidad es cuando, se crean nuevos nodos para que se adapten a la carga de trabajo. Esta es la forma más recomendada para hacer una buena escalabilidad.

  
## Principales Componetes 

 - PODS: Unidad mas pequeña que se puede desplegar y gestionar en kubernetes, en un grupo de uno o mas contenedores que comparte almacenamiento y red

 - Deployments: Describen el estado deseado  de una implementacion, ejecuta multimples replicas de la aplicacion,
 remplaza las que estan defectuosas o las que no responden 

 - Services: Definicion de como exponer una aplicacion que se ejecuta en conjuto de pods como un servicio de res, por lo general se usa roud-robin para balacear carga

 - Config Map: Permite desacoplar la configuracion para hacer la imagenes mas portables, almacenan variables de entorno, agumentos para lineas de comandos, o cofiguraciones de volumenes que pueden usar los pods.

- Labels: Pares de clave valor ('enviroment' : 'qa') para oragamizar, selecionar, consultar y monitoriar objetos de forma mas eficiente, ideales para UI Y CLIs.

- Selectorers: mecanismos para hacer consultas a las etiquetas .'kubectl get pods -l "enviroment in (production)" '


Arquitectura de Kubernetes: 

Kubernetes trabaja de forma que existe un nodo maestro que controla a todos los demas, nodo estos nodos controlados son llamados workers O Worker Machines

Kube-apiserver: Provee la interacion para las herramientas de administracion  Kubectl or Kubernetes dashboard.(Es el front end donde vamos a estar trabajando)

etcd: Almacenamiento que mantiene la configuracion y estado del cluster.

Kube-Scheduler: Al crear o escalar las aplicaciones el los nodos para los pods y ejecutar 

kube-controller-manager: Supervisa controladores mas pequeños que ejecutan tareas de replicar pods y manejar operaciones de los nodos. 
