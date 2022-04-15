# Kubernetes 

Es un sistema opensorce para la automatizar el despliegue, escalado y administración de aplicaciones en contenedores. También conocidos como  k8s (Pronounced Kate's).

Escalabilidad: capacidad de los sistemas para adaptarse al crecimiento por demanda y complejidad. 

- Tipos de Escalabilidad 
  -  Vertical:
      Este tipo de escalabilidad es cuando, en un mismo nodo nosotros lé aumentamos su procesamiento y  memoria. Esta forma no es para las más recomendable cuando la aplicación esta en crecimiento

  -  Horizontal:
     Este tipo de escalabilidad es cuando, se crean nuevos nodos para que se adapten a la carga de trabajo. Esta es la forma más recomendada para hacer una buena escalabilidad.

  
## Principales Componentes 

 - PODS: Unidad mas pequeña que se puede desplegar y gestionar en kubernetes, en un grupo de uno o mas contenedores que comparte almacenamiento y red

 - Deployments: Describen el estado deseado  de una implementación, ejecuta multiples replicas de la aplicación,
 remplaza las que están defectuosas o las que no responden 

 - Services: Definición de como exponer una aplicación que se ejecuta en conjugo de pods como un servicio de res, por lo general se usa roud-robin para balancear carga

 - Config Map: Permite desacoplar la configuración para hacer la imágenes mas portables, almacenan variables de entorno, argumentos para lineas de comandos, o configuraciones de volúmenes que pueden usar los pods.

- Labels: Pares de clave valor ('enviroment' : 'qa') para organizar, seleccionar, consultar y monitoriar objetos de forma mas eficiente, ideales para UI Y CLIs.

- Selectorers: mecanismos para hacer consultas a las etiquetas .'kubectl get pods -l "enviroment in (production)" '


Arquitectura de Kubernetes: 

Kubernetes trabaja de forma que existe un nodo maestro que controla a todos los demás, nodo estos nodos controlados son llamados workers O Worker Machines

Kube-apiserver: Provee la interaction para las herramientas de administración  Kubectl or Kubernetes dashboard.(Es el front end donde vamos a estar trabajando)

etcd: Almacenamiento que mantiene la configuración y estado del cluster.

Kube-Scheduler: Al crear o escalar las aplicaciones el los nodos para los pods y ejecutar 

kube-controller-manager: Supervisa controladores mas pequeños que ejecutan tareas de replicar pods y manejar operaciones de los nodos. 
