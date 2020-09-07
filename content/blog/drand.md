---
title: "Liga de la Entropía entra en etapa de producción."
author: CLCERT Universidad de Chile.
image: /img/posts/drand.png
date: "2020-08-11 12:00:05"
---

La Liga de la Entropía, una de las iniciativas donde participa [Random UChile](https://random.uchile.cl), entra en etapa de producción, convirtiéndose en el primer faro de aleatoriedad distribuido en convertirse en un servicio público de escala mundial. La U. de Chile se enorgullece de ser parte de esta iniciativa.

<!--more-->

## Drand: la máquina detrás de la Liga de la Entropía

Un Faro de Aleatoriedad Distribuido es un servicio que, al igual que Random UChile, genera periódicamente una cadena de bits aleatorios públicos, pero donde el algoritmo de generación es distribuido, esto es, requiere la participación de varias entidades. La [Liga de la Entropía](https://www.cloudflare.com/leagueofentropy/), es la primera red en proveer tal servicio, implementando para ello el algoritmo [drand](https://drand.love/).

Drand provee un mecanismo para la generación de aleatoriedad públicamente verificable, sin sesgo e impredecible. Su cálculo consiste en una fase inicial colectiva (una computación multipartita segura) para generar una llave distribuida entre los distintos participantes. Luego, en forma periódica y coordinada, cada uno de los participantes contribuye con datos que, al ser combinados entre sí, generan un valor al azar que puede ser consumido y verificado por cualquier usuario.

Drand comenzó como proyecto de investigación en [EPFL](http://dedis.epfl.ch/), y la primera red experimental se inició en el 2019 con la participación de Random UChile. Luego de un año de investigación y pruebas, el proyecto ha llegado a ser lo suficientemente maduro como para proveer un servicio robusto y confiable. Es así como hoy podemos anunciar el despliegue en producción de la red más grande que funciona con el sistema drand: la [Liga de la Entropía](http://leagueofentropy.com/).

## La evolución de la Liga de la Entropía

El verdadero poder de drand no viene solo de su implementación, sino de un diseño basado en una robusta y descentralizada red de nodos independientes que contribuyen a la generación de aleatoriedad. Es por ello que la actualización del sistema drand ha sido acompañada por un fortalecimiento de la Liga de la Entropía.

En sus orígenes en el año 2019, Cloudflare, EPFL, Kudelski Security, Protocol Labs y la Universidad de Chile aunaron esfuerzos para comenzar la Liga de la Entropía y ejecutar la primera red basada en el protocolo drand. Desde entonces, el grupo se ha expandido para incorporar a entidades repartidas en seis países, abarcando desde universidades hasta compañías privadas.

Los participantes de la Liga de la Entropía actualmente son:
- [C4DT](https://www.c4dt.org/)
- [ChainSafe](https://chainsafe.io/)
- [cLabs](https://celo.org/about)
- [Cloudflare](https://www.cloudflare.com/)
- [Emerald Onion](https://emeraldonion.org/)
- [EPFL](https://www.epfl.ch/labs/dedis/)
- [Ethereum Foundation](https://ethereum.foundation/)
- [IC3](https://www.initc3.org/)
- [Kudelski Security](https://www.kudelskisecurity.com/)
- [Protocol Labs](https://protocol.ai/)
- [PTisp](https://ptisp.pt/)
- [Tierion](https://tierion.com/)
- [UCL](https://www.ucl.ac.uk/)
- [Universidad de Chile](https://random.uchile.cl/)

## Modelo de Gobernanza de la Liga de la Entropía

Un factor fundamental en la robustez de esta red es el número y la diversidad de los nodos participantes. El protocolo Drand garantiza una aleatoriedad impredecible y segura donde ninguna entidad individual puede adquirir control total de la red; más aún, su seguridad depende de la ausencia de una coalición maliciosa mayoritaria. Esto sugiere la necesidad de un modelo explícito de colaboración, discusión y toma de acuerdos para la comunidad participante en la red.

La versión de producción de la Liga de la Entropía introduce un nuevo modelo de gobernanza donde se han establecido reglas y requisitos técnicos mínimos para cada uno de sus miembros, con el propósito de mantener un alto nivel de seguridad, además de asegurar la efectiva y correcta operación de cada uno de los nodos. La gobernanza además permite establecer las condiciones necesarias para mejorar constantemente la calidad del servicio entregado.

## Primer usuario de alto perfil: Filecoin

Todos los cambios y mejoras a la Liga de la Entropía han permitido conformar una red robusta y confiable de escala global. Un reconocimiento de esto es el reciente [anuncio](https://filecoin.io/blog/filecoin-testnet-phase-2-is-here/) del proyecto Filecoin (perteneciente a Protocol Labs) de adoptarla como su fuente de aleatoriedad oficial para la elección de líder en la Filecoin Blockchain. Tal uso contribuirá a una mayor innovación, testeo y desarrollo de la red en su conjunto.

## Relación con Random UChile

[Random UChile](https://random.uchile.cl) es un proyecto del [CLCERT](https://www.clcert.cl) de la Universidad de Chile para proveer un servicio de aleatoriedad pública, entregando aleatoriedad fresca cada minuto. Si bien provee un servicio similar a Drand (por ejemplo, en la Liga de la Entropía), tiene un par de diferencias relevantes. Primero, drand es un protocolo distribuido, y en consiguiente la aleatoriedad producida depende de la participación activa de diversas entidades durante su generación. La aleatoriedad generada por Random UChile, en contraste, es generada por una única entidad usando un algoritmo centralizado, aunque público y verificable. Para ello, para generar la aleatoriedad de cada minuto, Random UChile utiliza información obtenida de [diversas fuentes externas](https://random.uchile.cl/randomness-beacon/#fuentes) independientes (sismología, twitter, radio online y Ethereum) que aportan “frescura” a la aleatoriedad generada. En drand no existe ninguna contribución de fuentes externas al algoritmo de generación, por lo que su seguridad depende de la independencia y confiabilidad de los miembros de la red.

## Invitación a Seminario sobre Aleatoriedad

Con motivo de la nueva versión de drand y la puesta en producción del nuevo servicio, se realizará [The Randomness Summit](https://randomness2020.com/). Este evento tendrá lugar el jueves 13 de agosto, desde las 07:00 AM (hora chilena), y contará con diversas charlas y paneles con expertos de distintos países para hablar sobre drand, la Liga de la Entropía, y el futuro de los servicios de aleatoriedad pública. [¡Regístrate ahora!](https://airtable.com/shrTsIV4Btd8Wugqb)
