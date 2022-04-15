# Comando para controlar minikube 


## Comandos Principales

- Inicio del cluster 

`
 $ minikube start 
`

- Ver el status del  cluster 

`
 $ minikube status
`

- Detener el cluster 

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

- Mostrar la ip de la maquina

`
 $ minikube ip
`

- Exponer un servicio que el firewall no deja ver (windows)

`
 $ minikube server [server-name]
`


## Kubectl

-  Ver la version de la api 

`
 $  kubectl api-versions
`

- Aplicar archivos .yalm

`
 $ kubectl apply -f [FileName.yalm]
`

- Ver todo los desplegado

`
 $ kubectl  get all
`

- Borrar todos lo que esta dentro de una carpeta 

`
 $ kubectl delete  -f ./
`

- Desplegado todos lo que esta dentro de una carpeta 

`
 $ kubectl delete  -f ./
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
 $ kubectl delete pod [target]
`


- Ver información de un pods en especifico 

`
 $ kubectl  describe pod [target]
`

- Exponer el pod fuera del Cluster: 
    - Esto crea un servicio  

`
 $ kubectl expose pod  app type=loadBalancer --port=[puerto-exposición] --target-port=[default]
`
 

### Service 

- Obtener los servicios 

`
 $ kubectl get service 
`

- borrar un servicio 

`
 $ kubectl delete service [target]
`