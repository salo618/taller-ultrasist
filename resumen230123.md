Clase 23/01/23
=

Resumen
-

**se revisaron trabajos del fin de semana** aprendimos sobre las pruebas de unidad 

| Condiciones | Respuestas |
| ----------- | ----------- |
| Usuario vacio y password vacio | El usuario y el password deben ser no vacios |
| Usuario vacio y password no vacio | El usuario y el password deben ser no vacios |
| Usuario no vacio no valido y password vacio | El usuario y el password deben ser no vacios |
| Usuario no vacio valido y password vacio | El usuario y el password deben ser no vacios |


Conocimos la página swager que sirve para hacer pruebas de las funciones y ahorrar tiempo en las pruebas esta página hace creer a la página que estamos dando clic al botón de registrarse y nos va arrojando 
las posibles respuestas que nos devuelve la página.

**En esta pagina escogemos la funcion que deseamos validar.**

![image](https://user-images.githubusercontent.com/123017277/214195229-ab0a48de-7fd8-49b0-bf7f-9e7fb50be17e.png)

**En esta pagina nos arroja las respuesta que da la pagina.**

![image](https://user-images.githubusercontent.com/123017277/214196029-b9d8a79d-f574-479e-a341-2a4b926347c7.png)

instalamos el docker en la terminal de ubuntu usando los siguientes comandos

Docker es la tecnología en contenedores que permite crear y usar contenedores Linux

Las máquinas virtuales (VM) virtualizan (o eliminan la necesidad de administrar directamente) el hardware del servidor, mientras que los contenedores virtualizan el sistema operativo de un sistema. Docker es un sistema operativo (o runtime) para contenedores. El motor de Docker se instala en cada servidor en el que desee ejecutar contenedores y proporciona un conjunto sencillo de comandos que puede utilizar para crear, iniciar o detener contenedores.

- sudo apt install docker.io instalar docker
- sudo gpasswd -a ubuntu docker agregar al grupo
- apagar y encender la maquina virtual
- docker info

para correr el docker se utilizan los siguientes comandos
- docker pull ubuntu
- docker run -it ubuntu bash correr bash docker
- q salir
- apt update actualiza repositorios de bibliotecas
- apt install nano
- salir ctrl s   salir 
- docker run -it -p 80:80 nginx para correr el servidor local
- firefox local host
