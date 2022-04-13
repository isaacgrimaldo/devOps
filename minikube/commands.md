# Comando para controlar minikube 


## Comandos Principales

- Inicio del clouster 

`
 $ minikube start 
`

- Ver el status del  clouster 

`
 $ minikube status
`

- Detener el clouster 

`
 $ minikube stop
`

- Muestra el panel de control en el navegador

`
 $ minikube dashboard
`

- Expone un servicio estableciendo un puerto 

`
 $ minikube service [target]
`

## Kubectl

-  Ver la version de la api 

`
 $  kubectl api-versions
`


### PODS

- Crear un pod 

`
 $ kubectl run  [tag-pod]  --image=[docker-images] --port=[default] [new]
`

- Ver todos lo pods 

`
 $ kubectl get pods 
`

- Borrar un pod

`
 $ kubectl delte pod [target]
`


- Ver informacion de un pods en especifico 

`
 $ kubectl  describe pod [target]
`

- Exponer el pod fuera del Clúster: 
    - Esto crea un servicio  

`
 $ kubectl expose pod  app type=loadBalancer --port=[puerto-exposicion] --target-port=[default]
`
 

### Service 

- Optener los servicios 

`
 $ kubectl get service 
`

- borrar un servicio 

`
 $ kubectl delete service [target]
`