# Creación de microservicios y una canalización de CI/CD con AWS

### Índice
1. [Descripción del proyecto](#1-descripción-del-proyecto)
2. [Información sobre despliegue](#2-información-sobre-el-despliegue)
3. [Información sobre cómo usarlo](#3-información-sobre-como-usarlo)
4. [Autores](#4-autores)



## 1. Descripción del proyecto
Los propietarios de una corporación de cafeterías con muchas franquicias han notado que sus ofertas de café gourmet se han vuelto populares. 

Los clientes (los administradores de las franquicias de cafeterías) parecen no tener suficiente de los granos de café de alta calidad que son necesarios para crear increíbles capuchinos y lattes en sus cafeterías. 

Mientras tanto, los empleados en la oficina corporativa de la cafetería se han enfrentado al desafío de abastecerse constantemente con los granos de café de más alta calidad. Recientemente, los líderes de la oficina corporativa se enteraron de que uno de sus proveedores de café favoritos quiere vender su compañía. Los administradores corporativos de la cafetería aprovecharon la oportunidad para comprar la compañía. El proveedor de café que se adquirió ejecuta una aplicación de listados de proveedores de café en una cuenta de AWS, como se muestra en la imagen siguiente.

La aplicación de los proveedores de café se ejecuta, actualmente, como una aplicación monolítica. Tiene problemas de fiabilidad y rendimiento. 

Se pide dividir la aplicación monolítica en microservicios, de modo que pueda escalar los servicios de forma independiente y asignar más recursos de cómputo a los servicios que experimentan la mayor demanda, con el objetivo de evitar cuellos de botella. Un diseño de microservicios ayudará también a evitar los puntos únicos de error, los que podrían hacer caer toda la aplicación en un diseño monolítico. Con los servicios separados unos de otros, si uno de los microservicios está temporalmente no disponible, los otros microservicios podrían mantenerse disponibles.

Además, se tendrá también que desarrollar una canalización CI/CD para implementar automáticamente actualizaciones en el clúster de producción que ejecuta contenedores, utilizando una estrategia de implementación azul/verde. 

[:arrow_up:](#creación-de-microservicios-y-una-canalización-de-cicd-con-aws)

## 2. Información sobre el despliegue
Partimos de un escenario donde tenemos una VPC creada con 4 subredes, 2 públicas y 2 privadas. 
Estas se encuentran tanto en la zona de disponibilidad us-east-1a como us-east-1b. 

También disponemos de tres tablas de enrrutamiento, 2 para cada una de las privadas y otra para la pública que tiene salida por una puerta de enlace a internet.
En la subred pública 1, encontramos una EC2 que aloja nuestro servidor ubuntu 20.04 y que es la que guarda los archivos de nuestra aplicación monolítica.

La solución deberá de incluir los siguientes servicios o recursos en su diagrama:

- Amazon Virtual Private Cloud (Amazon VPC)

- Amazon Elastic Compute Cloud (EC2): instancias, equilibrador de carga de aplicación, grupos de destino

- AWS CodeCommit: repositorio

- AWS CodeDeploy

- AWS CodePipeline: canalización

- Amazon Elastic Container Service (Amazon ECS): servicios, contenedores, tareas

- Amazon Elastic Container Registry (Amazon ECR): repositorio.

- Entorno de AWS Cloud9

- AWS Identity and Access Management (AWS IAM): roles

- Amazon Relational Database Service (Amazon RDS)

- Amazon CloudWatch: registros

[:arrow_up:](#creación-de-microservicios-y-una-canalización-de-cicd-con-aws)

## 3. Información sobre como usarlo
La información para saber como usar este proyecto se puede encontrar en la wiki del repositorio, donde encontramos un [Manual de Despliegue](https://github.com/iesgrancapitan-proyectos/202324ASIR-Junio-Microservices-and-CI-CD-Pipeline-Builder/wiki/Manual_Despliegue#4-crear-dos-servicios-de-amazon-ecs) que explica como se ha realizado el proyecto paso a paso o el [Manual de Usuario](https://github.com/iesgrancapitan-proyectos/202324ASIR-Junio-Microservices-and-CI-CD-Pipeline-Builder/wiki/Manual_Usuario), donde explica lo que se tiene que hacer para el uso de este.

[:arrow_up:](#creación-de-microservicios-y-una-canalización-de-cicd-con-aws)

## 4. Autores
Guadalupe Luna Velázquez

[:arrow_up:](#creación-de-microservicios-y-una-canalización-de-cicd-con-aws)
