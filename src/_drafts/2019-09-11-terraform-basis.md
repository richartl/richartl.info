---
title: Terraform basis
categories:
- Infra
post_image: '/assets/blog/weeking_1/header.jpeg'
playlist: <iframe src="https://open.spotify.com/embed/user/22dbesvxgi7yutcssxnumbkwa/playlist/3a9hhanGedf9u7Ud0l4Tcl" width="100%" height="380" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>
---
Este pequeño post es un resumen de lo que es terraform y como podemos atacarlo de una manera màs fàcil para empezar a implementarlo. Como siemore trato en este tipo de material es ir al grano pero tambièn tratando de explicar con una pequeña analogìa que es y hace esta herramienta.

## ¿Què es terraform?

Terraform es una herramienta creada por Hashicorp (la misma compañia que ha creado herramientas como Vagrant y Vault) para automatizar y hacer màs fàcil la construcciòn (literalmente) de un ambiente completo en un proveedor de cloud (AWS, DigitalOcean, Google Cloud Plataform, Azure por mencionar a las màs populares) o plataformas (Heroku, Github entre otras) o el uso de otras herramientas (Docker, Vault, MySQL). Para consultar todo el stack de proveedores podemos hacerlo desde su [documentaciòn oficial](https://www.terraform.io/docs/providers/index.html).

La manera en la que trato de abstraer esta herramienta es literalmente construir infraestructura desde còdigo en un paradigma declarativo, es decir declaras literalmente lo que necesitas que se construya, el destino y metadatos y listo.

El lenguaje declarativo de esta herramienta puede parecer un poco extraño ya que es un lenguaje diseñado por Hashicorp llamado **Configuration Language**. Este lenguaje es muy sencillo y se usa de manera declarativa.

Una de las ventajas que da esta herramienta es, que puedes diseñar y construir toda tu infra en mòdulos que se pueden reutilizar ya que, como usas un lenguaje funcional puedes reutilizar el còdigo ademàs de parametrizarlo.

En pocas palabras esta herramienta abstrae todas las funcionalidades que brindan diferentes plataformas para su manejo por consola remota, es decir los clientes remotos como *awscli* de AWS y encima pone todo un framework para poder automatizar, agilizar, automatizar y versionar no solo la construcciòn de la infraestructura si no de su propio estado.

### Caso pràctico personal
Cuàndo tuve que migrar la infraestructura del sistema de una empresa en la que trabajaba primero optamos por hacer un pequeño laboratorio y pruebas de la arquitectura que habiamos propuesto. El primer paso era crear 3 diferentes instacias con diferentes pesos para poder desplegar ahi los microservicios que se tenian. El proceso para hacerlo era en un principio entrar a el panel de nuestro proveedor y de ahi crear las instancias que queriamos con las diferentyes caracteristicas que necesitabamos llamese zona, RAM, procesamiento y aparte agregarle las llaves para poder accesarlas. En nuestro proceso de despliegue se construyeròn y se destruyeròn al menos 5 veses las instancias, este proceso siempre era el mismo exceptuando cuàndo ajustabamos el tamaño de la instancia que en todo caso solo era cambiar el tipo de instancia.

Para este caso despuès descubrì que podìamos crear una receta con terraform que se puediera conectar a nuestro proveedor de cloud para tener todo versionado en còdigo y que con solo correr unos comandos en nuestra consola se podria crear y destruir instancias sin necesidad de entrar al panel de administraciòn web y hacerlo. En este caso la ventaja de usar la herramienta podrìa no parecer significativo ya que solo eran 3 instancias, pero imagine esto a una escala solo un poco màs grande como la de tener que replicar este diseño de infraestructura al menos unas 3 veses màs en otra zona de nuestro proveedor, eso si que nos huviera llevado mucho tiempo.

