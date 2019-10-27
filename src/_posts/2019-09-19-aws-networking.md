---
title: AWS Networking para dummies bien dummies
layout: post
featured_image: '/assets/images/posts/2019/aws_networking/header.jpeg'
featured_image_thumbnail: '/assets/images/posts/2019/aws_networking/header_thumbnail.jpg'
tags: [AWS]
---
Gracias a que hace casi un mes que cambie de chamba y que a su vez también cambié un poco de giro, es decir, cambié de un trabajo de desarrollo de software a uno en donde hay que meterle màs mano a la infraestructura de los proyectos y garantizar su confiabilidad y disponibilidad pues todo es nuevo para mi y con ello de regresa otra vez la ola de nuevo conocimiento herramientas y conceptos que pueden llegar a abrumar. Con esto no quiero decir que no me guste de hecho estoy tan emocionado y siguiendo mi pensamiento de que cuàndo enseñas algo puedes aprender màs que si solo estudias nació la inspitación para crear este post.

Esta va a ser la primera entrada de una serie en la que voy a tratar de explicar con un ejemplo muy sencillo lo que valla aprendiendo en mi estudio de AWS y sus servicios, en especial en esta serie me dedicaré a explicar temas que vienen en la certificación de Practitioner de AWS.

## Introducción
 Una de las cosas que se me hacìan muy complejas de todo el entorno de AWS y sus servicios era la parte de las redes. No se si a ti te pase lo mismo pero cuando estaba dentro de la consola de AWS o me hablaban de **Security groups** o **VPC´s** no sabìa que rayos. Bueno, en esta entrada trataré de explicar con un ejemplo muy sencillo y un poco tangible para los que vivimos en la CDMX.

 Puede que te guste o no te guste, te haga sentido o no, no digo que lo que valla escribir a continuación sea la verdad absoluta y que tengas que estar de acuerdo conmigo, si hay alguna observación o algo que pueda nutrir este ejemplo es siempre bienvenido. A mi defensa, *toy chikito y no puelo* gracias...

## Componentes de AWS
Con el siguiente ejemplo voy a tratar de explicar el concepto de los siguientes componentes de red de AWS:

* **IGW´s**
* **VPC´s**
* **Subnets**
* **Route Tables**
* **Network Access Control List**
* **Security Groups**

## Ejemplos

### VPC's y subnets

Podemos ver a una VPC como si fuera una ciudad completa, podemos decir que en una ciudad se encuentran otras minicudades que podriamos llamar municipios o alcaldìas, a estos últimos yo los relaciono como si fueran subnets.

![Subnets y VPC](/assets/images/posts/2019/aws_networking/vpc_subnets.png)

### IGW o Internet Gateways

La manera en que pude abstraer este componente es pensando en las casetas de cobro o los puntos de seguridad en la principales accesos a una ciudad. Digamos que la informaciòn fluye de adentro de la ciudad hacia afuera y viceversa. Digamos que cuàndo las personas fluyen de adentro de la ciudad hacìa afuera se hace referencia a cuànde desde dentro de una VPC fluye informaciòn hacia internet.

![IGWS](/assets/images/posts/2019/aws_networking/igws.png)

### Route tables

Este elemento yo lo comparo con la configuraciòn o direcciones que podemos seguir para llegar a cierto lado, puede que ciertos caminos nos lleven a un lugar y hay otros que definitivamente no nos llevarìan a el lugar deseado. Serìa como nuestro GPS que nos va diciendo que camino tomar.

![Route Tables](/assets/images/posts/2019/aws_networking/route_tables.png)

### Network Access Control List

Este elemento se podrìan abstraer como las polìticas o reglas que se usan para poder acceder a una subnet o miniciudad, en este caso se podrìa tratar como los medios por los cuàles puedes ingresar a esta, caminando, en carro, si es en carro con ciertos permisos, si es caminando con ciertas credenciales, etc...

Por ejemplo a una terminal de autobuses un usuario puede entrar caminando y si va hacia afuera de la ciudad no va a salir caminando. Puedes entrar al metro caminando y salir caminando pero no sales en automovil.

![NACLs](/assets/images/posts/2019/aws_networking/nacls.png)

### Security Groups

Los security groups son un filtro pero dentro de las subnets, es decir serìan un filtro para entrar a ciertos lugares de una miniciudad, en caso del metro para entrar a las estaciones necesitas pagar, en el caso de una central camionera debes pagar para subir a cierto camiòn y pagar màs para subir a uno màs largo o còmodo.

![Security Groups](/assets/images/posts/2019/aws_networking/security_groups.png)

### Redes privadas y pùblicas

Una red pùblica es una que tiene acceso al exterior, una privada solamente tiene comunicaciòn dentro de la VPC, esto lo podemos comparar con una central camionera, etsa tiene medios para comunicarse hacia el exterior, si lo comparamos con un transporte como el metro, que solamente tiene comunicaciòn dentro de la ciudad y hacia la central camionera pero no hacia el exterior.


![Complete](/assets/images/posts/2019/aws_networking/complete.png)
