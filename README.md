# Nueva página del CLCERT

Este repositorio representa los archivos fuente de Hugo que generan la página principal del CLCERT.

A continuación, un pequeño resumen/instructivo de como modificar la información del sitio:

## Consideraciones generales

Para editar el contenido de los archivos que terminan en `.md`, hay que seguir las reglas del lenguaje [Markdown](https://guides.github.com/features/mastering-markdown/). En el caso de los archivos que terminan con `.html`, es posible escribir HTML tradicional.

## Agregar estudiantes de diplomado

Para agregar estudiantes de diplomado, es necesario hacer 2 cosas:
 - Agregar las fotos de los estudiantes de diplomado a `static/img/diplomados/<año>/`. **Se recomienda que tengan un tamaño de 128x128 pixeles**.
 - Agregar un archivo por cada año a la carpeta `data/diplomados/` en formato `.yaml`. Dentro de este archivo se agregan secuencialmente los estudiantes del diplomado, llenando los siguientes campos:

 ```yaml
- nombre: Juan
  apellido: Pérez
  foto: jperez.jpg
 ```

 * El campo `nombre` representa el nombre del ex alumno.
 * El campo `apellido` representa el apellido del ex alumno.
 * El campo `foto` representa el nombre de la foto del ex alumno.

Recordar que solo el campo `nombre` lleva un guión y luego un espacio al inicio. Los otros campos llevan 2 espacios seguidos. Es importante seguir esta convención.


## Agregar proyectos

Para agregar proyectos y convenios, es necesario hacer 2 cosas:

 - Agregar la foto del proyecto a `static/img/proyectos/`. **Se recomienda que tengan un tamaño de 640x480 pixeles**.
 - Editar según tipo de proyecto (Proyectos Actuales, Convenios, Proyectos anteriores) el archivo respectivo en la carpeta `data/proyectos/`. Dentro de este archivo se agregan secuencialmente los proyectos, llenando los siguientes campos:

 ```yaml
  - nombre: Observatorio de Seguridad de la red
    imagen: osr.svg
    url: https://osr.cl
    descripcion: Proyecto que busca monitorear continuamente la red chilena
    oculto: true
    destacado: true
 ```
* El campo `nombre` representa el nombre del proyecto.
* El campo `imagen` representa el nombre de la imagen del proyecto, ubicada en la ruta anteriormente mencionada.
* El campo `url` representa el enlace al cual lleva el proyecto. En general lleva a la página del proyecto o a un blog post anunciándolo.
* El campo `descripción` describe muy brevemente (<8 palabras) el proyecto.
* El campo `oculto` oculta el proyecto de la página final. Sirve para proyectos que no se quieren publicar todavía.
* El campo `destacado` muestra el proyecto en la página inicial.

## Agregar Integrantes del equipo


Para agregar integrantes, es necesario hacer 2 cosas:

 - Agregar la foto del proyecto a `static/img/integrantes/`. **Se recomienda que tengan un tamaño de 600x600 pixeles**.
 - Editar según tipo de integrante (Permanente, tesista, memorista, practicante) el archivo respectivo en la carpeta `data/proyectos/`. Dentro de este archivo se agregan secuencialmente los integrantes, llenando los siguientes campos:

 ```yaml
    - nombre: "Alejandro Hevia"
      cargo: "Director"
      github: "ahevia"
      twitter: "ahevia"
      web: https://users.dcc.uchile.cl/~ahevia
      foto: "ahevia.jpg"
      bio: "Académico del Departamento de Ciencias de la Computación, U. de Chile"

 ```
* El campo `nombre` representa el nombre del integrante.
* El campo `cargo` representa el subtítulo del nombre del integrante. Este valor generalmente es el cargo o el año de la tesis/memoria.
* El campo `github` representa el nombre de usuario en GitHub del integrante.
* El campo `twitter` representa el nombre de usuario en Twitter del integrante.
* El campo `web` representa el sitio web del integrante.
* El campo `foto` contiene el nombre de la foto subida anteriormente.
* El campo `bio` contiene una breve biografía o descripción.
 
## Agregar Entradas de Blog a la portada

Para agregar entradas de blog a la portada, basta con crear el archivo de la entrada nueva en la carpeta `content/blog`.  Aparecerán las 3 publicaciones más recientes en inicio, y se podrán ver todas en la pestaña "Blog". El archivo blog tiene que tener la siguiente cabecera:

```yaml
---
title: "Estudio: Al menos 2.933 dispositivos afectados por BlueKeep expuestos en la red chilena."
author: CLCERT Universidad de Chile.
image: /img/posts/old_lock.jpg
date: "2019-05-19 20:30:40"
summary: "Esta semana realizamos un estudio de ciberseguridad de la red chilena, el cual revela la existencia de un número importante de computadores conectados a la Internet afectados por la vulnerabilidad [**CVE2019-0708**](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-0708), también conocida como _BlueKeep_."
---

Cuerpo del post
```

* El campo `title` es el título del post.
* El campo `author` es el autor del post.
* El campo `image` corresponde a la foto principal del post.
* El campo `date` posee la fecha de publicación del post, en formato YYYY-MM-DD HH:MM:SS.
* el campo `summary` contiene un resumen del post, en caso de existir. Si no, este se calcula manualmente a partir del cuerpo del post.

## Agregar post de Humor

La mecánica es muy similar a la de agregar entradas de blog a la portada:
 - Primero, es necesario agregar la foto relacionada con el artículo de humor (en caso de existir) a `/static/img/humor/`.
 - Después, es necesario escribir el `artículo` en la carpeta `"content/humor/`. La estructura interna del archivo debe partir así:

```yaml
---
title: Ataque de Diccionario
date: 2018-09-01
image: dictionary-attack.jpg
creditName: Fuente 1
creditLink: https://clcert.cl
---
`Contenido del post, va después de la imagen`
```

* El campo `title` es el título del post de humor.
* El campo `date` define la fecha del post de humor.
* El campo `image` contiene la imagen del post de humor. Es opcional
* El campo `creditName` contiene el nombre de la fuente.
* El campo `creditLink` contiene el enlace a la fuente del post.
* Bajo los 3 guiones inferiores, va el contenido del post (de existir), escrito en markdown

Es completamente necesario colocar los 3 guiones al inicio del archivo y justo antes del contenido del post (o al final del archivo si el post no tiene contenido).

## Editar contenido de páginas

Dentro de la carpeta `content/`, todo lo que no es `humor` y `blog`corresponde a las páginas del sitio. 

## Subir sitio a producción

* Guardar cambios en Git
* ejecutar comando `hugo` en la raíz del proyecto
* Copiar archivos generados en `/public/` al servidor.

## Estadísticas

Las estadísticas fueron retiradas del sitio principal del CLCERT, ya que serán manejadas por el sitio del OSR.

 # Por hacer en el sitio
  - Actualizar la historia (no se toca desde 2007)
  - Completar info de integrantes
  - Automatizar el deployment del sitio cada vez que se modifica algo
  - Mejorar la visualización en móvil
