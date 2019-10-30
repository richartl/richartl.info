---
layout: post
title: La historia detrás del mito, DevOps
tags: [DevOps]
featured_image: '/assets/images/posts/2019/devops_essentials/header.png'
featured_image_thumbnail: '/assets/images/posts/2019/devops_essentials/header_thumbnail.png'
---
El mundo de la técnología y el desarrollo se mueve a un velocidad estrepitósamente rápida, pensemos en que la industria de la computación en sus diferentes áreas aplicadas no lleva más de 50 años de haberse consolidado. Casi 2 generaciones vierón como el mundo evolucionaba gracias a ella y en algún aspecto de la vida común de la sociedad se fué permeando poco a poco tanto que ahora se nos hace difícil pensar como se pudo haber vivido sin ella hace muchos años. El simple hecho de que estes leyendo y yo pueda compartir esta entrada frente a tu pantalla es un reflejo de esto. GRACIAS INTERNET!

Si nos ponemos a pensar por ejemplo (y es algo que a mi me sirve mucho de referencia personal) el simple hecho de tener una computadora o teléfono celular personal es un reflejo de eso. Recuerda las primeras computadoras, recuerda los primeros teléfonos celulares, ¿Recuerdas tu primer computadora?, ¿Recuerdas tu primer teléfono celular?, ¿Cómo era?, ¿Qué características tenía?, ¿Recuerdas hace cuánto fué que lo tenías?. En la mayoria de los casos, desde nuestro primer computadora o teléfono celular hasta el que tenemos ahora no habrán pasado más de 15 años. En 15 años cuánto ha mejorada, si los comparámos uno del otro la diferencía de técnologías es abismal.

Uso esta referencía para poner un contexto de lo que sigue, hay compañias hoy en día que han basado todo su exito en tecnologías como el internet y los teléfonos celulares, de hecho es una tendencía. Compañias como Uber, Amazon, Facebook, Google tienen por pilar principal de estas desarrollos técnologicos que les dan su fuerza competitiva.

Como pilar principal los desarrollos tecnológicos deben cumplir ciertas carácteristicas para que estas compañias puedan mantenerse en el mercado, 2 de las que considero las más importantes son:

* *Velocidad*: El tiempo que te tardas en realizar una nueva funcionlidad o innovación a tu producto, desde que lo estas desarrollando hasta que esta disponible para los usuarios finales.
* *Estabilidad*: Una vez que hayas liberado la nueva funcionalidad o innovación, la confiabilidad que tienen los usuarios de poder usarla sin fallas y su disponibilidad.

Dejando un poco de lado como tal la innovación que si bien, es y ha sido importante en la industría en mi punto de vista pertenece a una etapa o proceso preliminar al que trato de abordar en esta entrada. ¿Qué huviera pasado si Uber huviera revolucionado la manera de transportarse pero la plataforma fuera inestable, ¿huviera tenido exito?

Teniendo en cuenta las 2 caracteristicas anteriores hoy en día se puede medir la eficiencía y confiabilidad de una compañia desde el ámbito legal hasta la adopción de los usuarios finales.

En la prehistoria del desarrollo de software, un procentaje muy alto de los proyectos de desarrollo o más bien la mayoria de ellos no llegaban a fin, tardaban años en salir a la luz y cuándo lo hacian los requerimientos de estos no cumplian con los requerimientos y si lo hacían estos ya no eran sufucientes, claro! después de 2 años de desarrollo las condiciones y requerimientos seguro ya no eran las mismas.

A raíz de esto nacierón las MÉTODOLOGIAS ÁGILES DE DESARROLLO DE SOFTWARE... si se escucha muy espectacular, a eso quería llegar y sí, realmente fue un espectacular cambio de paradigma de como hacer las cosas en el desarrollo de software.

A resumidas cuentas lo que vino a cambiar estas metodologías fué:
* Centrarse hacer, hacer, hacer! más que en perder tiempo en planeación
* No tener un marco de trabajo tan rígido en cuánto a los requerimientos
* Dar por hecho que las prioridades del desarrollo podrían cambiar
* Periodos cortos de desarrollo (máximo 4 semanas) y muchas iteraciones
* El resultado de cada iteración debe ser un producto estable y usable pora los usuarios finales
* Las prioridades y nuevas funcionalidades deben ser basadas en la experiencia de los usuarios al utilizar el producto, es decir, el feedback y los siguientes pasos siempre son a partir de la experiencia de estar usando el productoi que estas creando y aqui es donde nace el *Minimum Viable Product* o *MVP*

Este nuevo paradigma de hacer las cosas ayudó mucho a brindar competitividad a las compañias en donde uno de sus pilares era un producto técnologíco. Aquí es donde me llega la pregunta, ¿El tener un marco de trabajo en donde la velocidad de desarrollo era más rápida hizo que las compañias consideraran basar su competitividad en productos tecnológicos o basar su competitividad en productos tecnológicos hizo que se crearan marcos de trabajo ágiles?. En mi opinion, fué parte de las 2.

A partir de este nuevo marco de trabajo se fuerón perfilando ciertos roles para cumplir determinadas tareas, por una parte lo desarrolladores (Devs) que son los encargados de hacer las nuevas funcionalidades y tirar todas las lineas de código necesarias para cumplir estos objetivos, en este punto, se crearón muchas nuevas herramientas, lenguajes y frameworks para cumplir la nueva demanda de productos de software. Por otro lado nacío el rol de QA, el encargado de hacer el testing de las funcionalidades que creaban los Devs, para esta labor también se crearón nuevas herramientas, metodologías y frameworks para llevar esto a cabo. Y por último pero no menos importante, se especializó el rol de operaciones (Ops), los encargados de tener a punto toda la infraestructura en la cuál desplegar y poner disponible los productos de software, este rol es comúnmente llamado SysAdmin, igual que los otros roles, este se fué especializando y creando herramientas para cumplir su trabajo.

Estos roles formarón por mucho tiempo la estructura de un equipo de desarrollo, Devs, QA Testers y SysAdmins. Cada uno especializado en su labor y sin necesariamente conocer el trabajo de los otros.
Sobre esta estructura el flujo normal del despliegue de una nueva funcionalidad era:
* Los desarrolladores creaban o mantenian funcionalidad del producto de software
* Los QA testers realizaban la labor de probar los nuevos cambios y dar un veredicto.
* Los SysAdmin se encagaban de desplegar sobre su infraestructura la nueva funcionalidad.

Esto parece un buen flujo, lo era, pero la velocidad y estabilidad se veían comprometidas debido a un fenómeno que ocurria entre estas áreas o roles. THROW OVER THE WALL!!

Este fenómeno llamado así por la acción de aventar algo sobre el muro, olvidandose y delegando la responsabilidad a la persona del otro lado del mismo. Es decir, los devs creaban la nueva funcionalidad y **aventaban** y delegaban la responsabilidad a la siguiente zona sin tener comunicación alguna de los requerimientos que sus compañeros necesitaban para poder probar esto, en muchos casos estos **aventaban** la responsabilidad de regreso a los dev, en otros casos **aventaban** esta responsabilidad sobre el siguiente muro, a los SysAdmins y la acción se podria repetir **aventando** la responsabilidad de muro en muro, afectando directamente la eficiencía y agilidad que se suponia debia de ser.

Estas prácticas y naturalmente afectaban también a la coordialidad que debía existir en estos equipos, el señalar con el dedo era una práctica común una vez algo salía mal y la interminables juntas de revisión no ayudaban a mejorar esto. Ego, hostilidad, malos entendidos, son los ingredientes necesarios para el fracazo de cualquier proyecto y malos equipos, sin mencionar que, los productos de software se retrasaban en el mejor de los casos y en los peores costaban muy caro a las empresas.

![dilema](/assets/images/posts/2019/devops_essentials/common_problem.png)

Este caso era el ideal para que una **revolución** se diera. Y... se dió.

El término DevOps nace de tomar parte de 2 palabras:
* *Dev* = Developers
* *Ops* = Operaciones (sysadmin)

De estas 2 nace *DevOps*, si, así de fácil y práctico. Pero, ¿Qué es DevOps? ...

Contestando esto con otra pregunta... *¿Qué no es DevOps?*

*DevOps* no es:
* Una carrera
* Un título o puesto de trabajo
* Un producto
* La nube o cloud
* Una serie de herramientas
* Un standard de la industria

*DevOps* es:
* Una cultura
* Una filosofía de trabajo
* Una serie de buenas prácticas

No existe un cargo DevOps más bien hay personas que práctican DevOps, no es una serie de herramientas, DevOps crea herramientas, pero no las herramientas hacen al DevOps, DevOps crea standares y no lo contrario, DevOps hace uso de la nube pero no necesariamente la nube es DevOps.

Este movimiento nació en 2009 gracias a personas que eran consientes de estos problemas y los males que estos causaban. Patrick Debois y Andrew Shafer iniciarón este movimiento, movimiento que cada año crece más y se especializa más. Solo falta ver el número de DevOpsDays que se llevan a cabo mundialmente cada año. Las herramientas que cada vez se especializan y se crean.

Pero, ¿Cómo es que este movimiento ayudó a mitigar estas prácticas?

Si lo ponemos en perpectiva, este problema se daba debido a que los objetivos de cada rol era opuestios en si. Mientras el objetivo de los desarrolladores era la velocidad, el objetivo de los sysadmin era la estabilidad. Mientras los unos querían poner el mayor número de features posibles disponibles para los usuarios finales, los otros tenían que garantizar la disponibilidad y estabilidad del producto. Los cambios son la principal causa de errores en los sistemas, entonces he aquí el dilema.


![Contrary Goals](/assets/images/posts/2019/devops_essentials/goals_contrary.png)

Con DevOps surgen formas para garantizar la velocidad de crear nueos features y ponerlos a la disponibilidad de los usuarios finales conservando la estabilidad del producto. Con prácticas como TDD, integración contínua, despliegues continuos, monitoreo entre otras DevOps resultó ser el siguiente paso a seguir para mejorar la industría.


![DevOps Goals](/assets/images/posts/2019/devops_essentials/goals_devops.png)

Realmente no hay perfección alguna, siguen habiendo errores aunque la realidad es que cada vez menos y con un tiempo de reacción muy rápido. Se tiene más control sobre cada release y con esto se da fuerza competitiva a las compañias y productos.

## Recursos

* [Presentación](https://docs.google.com/presentation/d/1TOr4sHgrWG4RAeZAJetKXNJYpF6v7hkXanTPxLQgq8g/edit?usp=sharing)
* [DevOps Essentials Course by Linux Academy](https://linuxacademy.com)
* [New Relic DORA report](https://blog.newrelic.com/technology/dora-accelerate-state-of-devops-2019/)
