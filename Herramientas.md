# Sobre los lenguajes y herramientas que utilizaremos

Cualquier _workflow_ editorial es en esencia un conjunto de tareas sincronizadas, realizadas cada una con herramientas específicas, donde se manipula texto, información sobre ese texto e información gráfica en orden a  producir un libro. Para manipular ese texto, un ordenador (o el software instalado en ese ordenador) necesita que el texto esté etiquetado  semánticamente. Esto suena complejo, pero solo significa que si tenemos un documento, ese documento debe también incluir información acerca de cual es el título, cual es el autor, que función tienen los diversos párrafos (¿acaso son cuerpo de texto, epígrafes, citas?). Para describir esa información, existen lenguajes de etiquetado.

## lenguajes

Esta información la trasladamos al documento en forma de etiquetas y tienen este aspecto:

````
<h1>Este es el título de mi documento</h1>
<p>Este es un párrafo y en este párrafo hay una cita textual: <q>nunca digas nunca jamás</q>
````
En este extracto, lo que hay es un título (lo que está entre las etiquetas `<h1> y </h1>`, `h1` por `heading 1` o bien: título principal de de primer nivel), un párrafo (lo que está entre las etiquetas `<p> y >/p>`), una cita (lo que está entre las etiquetas `<q>` y `</q>`, donde `q` significa quotation, o sea: cita textual. Y esta información permite que este texto pueda ser interpretado por maquinas (esto es lo que ocurre cuando un navegador despliega en pantalla una página web: toma información de una fuente determinada y la transforma en un documento web siguiendo la estructura que definen sus etiquetas y la información gráfica que viene en su CSS. Esto último lo veremos más adelante. ).

Pero el HTML es algo engorroso y pese a que hay herramientas extrordinarias que facilitan su escritura, tenemos una posibilidad mejor: trabajar con texto siguiendo la sintaxis markdown, que simplifica mucho el trabajo. De manera que el trozo anterior sería (escrito en markdown) más bien así:

````
# Este es el título de mi documento

Este es un párrafo y en este párrafo hay una cita textual: *nunca digas nunca jamás*.
````
Mucho más fácil, ¿verdad? Además tiene varias ventajas:

1. Estamos etiquetando texto de tal manera que lo pueda entender un software, pero manteniendo su legibilidad para cualquier humano que decida echarle un vistazo.
2. Se puede transformar en otras sintaxis (otros lenguajes de etiquetado), mas complicadas, de forma automática (en efecto, markdown fue ideado para escribir HTML de manera rápida)
3. Es [extremadamente ligero](/wordVersusMarkdown.md)

De manera que el lenguaje (o la sintaxis) de etiquetado que utilizaremos en primer término será markdown, y en fases más avanzadas: HTML y CSS (cuando hablemos de un archivo EPUB), y Liquid y JavaScript (cuando creemos nuestra primera página web con la información de un libro).

## Herramientas

En cuanto a las herramientas, las vamos a escoger siguiendo los siguientes criterios:
- que sean multiplataforma (o sea, que tengan versiones disponibles para cualquier sistema operativo)
- que sean fácilmente configurables
- que se integren bien entre ellas
- la navaja de Ockham: que sean la solución más simple para los problemas que tenemos que resolver
- Y que preferiblemente sean Open Source

### Editores de texto

Para escribir Markdown y todos los lenguajes con los que trabajaremos, necesitaremos un editor de texto. Hay muchos, pero para el caso que nos ocupa, vamos a considerar flujos de trabajo con Atom y Visual Studio Code, los dos multiplataforma y gratuitos. También necesitaremos usar el terminal (en Mac y Linux) o La Power Shell(en Windows) para determinadas acciones. veremos en articulos separados cómo configurarlos.


### Para manipular el texto

Una sola herramienta nos servirá para convertir nuestro texto formateado como markdown en HTML (para reutilizarlo en la construcción de nuestro preview para la web), en EPUB (como formato de Ebook para retailers como Kobo o IbookStore o Google Play), para importarlo en InDesign (vía ICML), para convertirlo en Docx (si es que por alguna razón queremos hacer semejante cosa). Esta herramienta se llama Pandoc.

### Para colaborar y hacer control de versiones

Usaremos Git y GitHub, el uno, un software de control de versiones, la segunda, una plataforma organizada por repositorios y construida para colaborar en proyectos utilizando Git como herramienta de control de versionjes y colaboración. Github nos servirá también para construir y alojar nuestra página web.

### Para construir nuestra web (y nuestra tienda electrónica)

usaremos jeckyll, un software que permite crear sitios webs estáticos en cuestión de segundos, y Liquid, el lenguaje en que están escritas las plantillas de Jeckyll y de Shopify (que es el software que utilizaremos para construir nuestra plataforma de ecommerce).
