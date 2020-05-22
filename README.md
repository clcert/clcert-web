# Nueva página del CLCERT

Este repositorio representa los archivos fuente de Hugo que generan la página principal del CLCERT.

A continuación, un pequeño resumen/instructivo de como modificar la información del sitio:

## Consideraciones generales

Para editar el contenido de los archivos que terminan en `.md`, hay que seguir las reglas del lenguaje [Markdown](https://guides.github.com/features/mastering-markdown/). En el caso de los archivos que terminan con `.html`, es posible escribir HTML tradicional.

## Agregar estudiantes de diplomado

Para agregar estudiantes de diplomado, es necesario hacer 2 cosas:
 - Agregar las fotos de los estudiantes de diplomado a `/assets/img/alumni/<año>/`. **Se recomienda que tengan un tamaño de 128x128 pixeles**.
 - Agregar un archivo por cada año a la carpeta `data/alumni/` en formato `.toml`. Dentro de este archivo se agregan secuencialmente los estudiantes del diplomado, llenando los siguientes campos:

 ```toml
 [[alumni]]
 first_name = "Eduardo"
 last_name = "Riveros"
 photo = "eriveros.jpg"
 ```
 
## Agregar post de humor

La mecánica es muy similar a la de agregar estudiantes de diplomado:
 - Primero, es necesario agregar la foto relacionada con el artículo de humor (en caso de existir) a `/assets/img/humor/`.
 - Después, es necesario escribir el `artículo` en la carpeta `"_humor/`. La estructura interna del archivo debe basarse en la de publicaciones anteriores, definiendo un título para el post, una imagen, contenido (bajo el header de los `---`
) y los créditos del contenido (Link y texto).


## Agregar Entradas de Blog a la portada

Para agregar entradas de blog a la portada, basta con crear el archivo de la entrda nueva en la carpeta `content/blog`.  Aparecerán las 3 publicaciones más recientes en inicio, y se podrán ver todas en la pestaña "Blog".

## Editar contenido de páginas

Dentro de la carpeta `content` se encuentran las páginas del sitio. 

Es muy importante notar que **es necesario seguir una estructura específica en el encabezado del archivo para que las subpáginas sean reconocidas como tales**. Esta estructura es metainformación que va entre 2 líneas con 3 guiones (`---`) en el encabezado de cada archivo. Se recomienda ver los ejemplos ya existentes para replicar esa metainformación y adecuarla según sea el caso.

## Subir sitio a producción

Luego de hacer el commit/push a master de este repositorio, basta con ingresar a despliegue1 y ejecutar `./update_website.sh`

## Estadísticas

Las estadísticas fueron retiradas del sitio principal del CLCERT, ya que serán manejadas por el sitio del OSR.

 # Por hacer en el sitio
 - Actualizar sección "nosotros"
  - Actualizar la historia (no se toca desde 2007)
  - Actualizar los integrantes con gente que trabaja y ha trabajado en el CLCERT (Y agregar fotos si se puede)
  - Agregar una nueva sección "Proyectos" con links e info de los proyectos actuales y pasados.
 - Automatizar el deployment del sitio cada vez que se modifica algo
 - Mejorar la visualización en móvil
