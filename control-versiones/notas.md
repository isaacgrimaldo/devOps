# Notas del Control de versiones

Git => Es sistema de gestión de versiones distribuido, opensource y se puede integrar con diferentes repositorios. Algunos ambientes donde se utiliza (Gitlab,  GitHub, Bitbuket);

## Git trunk Based

Esta una forma de trabajar en una sola rama principal

### Pasos:

-  Crear una rama principal donde se crearan la base del proyecto
-  Crear un branch para empezar crear las nuevas funcionalidades
-  Después de aver creado las nuevas funcionalidades de puede hacer 
   merge al rama principal, claro si el código paso todos los procesos de testing 
-  Recordad siempre hacer un git pull  o un rebase para tener el     repositorio siempre actualizado 

### Ventajas
   
   Trunk based: Estándar usado para equipos de ingeniería de alto rendimiento

- 1. Es una practica requerida para integración continua
- 2. Cuando se esta iniciando un proyecto
- 3. Cuando el equipo de desarrolladores principalmente esta integrado por seniors
- 4. Cuando el equipo requires iterar rápido
- 5. Cuando se trabaja con un equipo de TDD


## Git Flow

Esta forma de trabajar es con 5 niveles de ramas.

### Ramas

- 1. master => Almacena el historial de versiones oficiales, nunca recibe código directo 
- 2. develop: Funciona como rama de integración  de las features, nunca recibe código directo
- 3. feature: Parte de develop , son temporales, es qui donde los desarrolladores agrega código  de nuevas características 
- 4. release: Parte de develop, preparación de la release, se despliega en entornos del pruebas, se hace ajustes y se integra en mater y  develop  (release:x.y.z)
- 5. hotfix: Parten de master, para arreglar errores urgentes, se integran en master y dev y  se marcan como versiones con tag. (hotfix:x,y,z)  


### Ventajas
   
- 1. Indicada para proyectos open source 
- 2. Cuando el numero de desarrolladores junior es alto
- 3. si el indice de rotación del equipo es alto
- 4. Cuando se cuenta con un producto establecido (En producción)
- 5. Calendario de releases fijo 




## Conceptos Importantes

Trunk : Es la línea base del repositorio 

Branch : Nueva bifurcación del estado actual del código  que crea una nueva 
ruta para evolucionarolo

Fork: Duplica el repositorio y su historial

Tag: Etiqueta para identificar versiones 
