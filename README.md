# is-api

Se requiere implementar un backend con un API Rest (Java Funcional) que reciba un array de arrays de números que conformen una matriz de NxN representando una imagen, y se devuelva la misma matriz que represente la imagen, pero rotada en sentido anti-horario (90 grados). La API debe ser de tipo POST, el Content-Type de los request y response deben ser application/json y se debe controlar correctamente los errores. Adicional, el backend debe estar dockerizado. Considerar que esta primera versión será la base para que posteriormente otros desarrolladores puedan incluir los demás endpoints que aún están en definición, por lo que la solución debe garantizar la mantenibilidad y escalamiento.

## Instalación
```sh
mvnw install
mvnw package
```
## Ejecución
### JAVA
```sh
java -jar target/test-0.0.1-SNAPSHOT.jar
```
### DOCKER
```sh
docker build -t is-api .
docker run -p 8080:8080 is-api
```

## Ruta para rotar matriz
### POST
http://localhost:8080/matrix/rotate