# markdown

## ¿Qué es Markdown?

Es un lenguaje de marcado (o etiquetado) semántico creado por John Gruber y Aaron Schwartz en 2004 y su propósito original era proveer de una herramienta de conversión de texto a HTML para escritores web. Pero con el tiempo se ha transformado en una especie de lengua franca de internet. Muchos servicios web y la mayoría de los CMS lo aceptan y hasta es posible (pero eso lo veremos más adelante) escribir una página web utilizando Markdown, algún software y unos cuantos clics. Markdown permite escribir utilizando un formato de texto plano fácil de leer y escribir, y luego convertirlo a XHTML (o HTML) estructuralmente válido [más info](https://es.wikipedia.org/wiki/Markdown). Lo crucial es que Markdown es una convención para estructurar tus documentos en *texto plano* de una manera semántica. La idea es identificar estructuras lógicas en tu documento (un título, una sección, subsecciones, notas al pie, etc.), marcarlas con algunos caracteres distintivos y luego “compilar” el texto resultante con un intérprete de composición tipográfica que dará forma al documento en consonancia con el estilo especificado.

## ¿Por qué utilizar Markdown?

1. Markdown te obliga a escribir para la web. O también (pero mejor): MD te obliga a concentrarte únicamente en la estructura del texto. A diferencia de MS Word, Markdown fue concebido con el objetivo de ser ligero, flexible y estructurado: escribir en markdown te obliga (o al menos, lo hace más fácil) a enfocarte en el significado de tu texto y en las estructuras semánticas que lo sostienen.

2. Es un formato transparente. Word o, ya que estamos, cualquier procesador de texto, consiste en varias capas. La que ves (su interfaz gráfica) es donde escribes y le das formato al texto, pero debajo hay una capa que interpreta lo que tu escribes (y el formato que le das a lo que escribes) y la codifica. Este código no sólo es totalmente ilegible, sino que es extremadamente enrevesado, lo cual amplifica lo posibilidad de error cuando se transfiera el archivo a otro software que a su vez tendrá que interpretar ese código. (esto es importante retenerlo: cualquier software genera e interpreta código y mientras más limpio, liviano y estructurado sea este, más fácil es que pueda pasar de un software a otro sin errores)

3. Que sea transparente equivale a decir que se puede almacenar en un archivo de texto plano. Esto supone que se puede abrir en prácticamente cualquier disposito presente, pasado o futuro.

## Una breve guía de etiquetado de texto en Markdown

Markdown es una convención para estructurar tus documentos en texto plano de una manera semántica. La idea es identificar estructuras lógicas en tu documento (un título, una sección, subsecciones, notas al pie, etc.), marcarlas con algunos caracteres distintivos y luego “compilar” el texto resultante con un intérprete de composición tipográfica que dará forma al documento en consonancia con el estilo especificado. También, como ya veremos, se puede utilizar markdown para crear un documento base que InDesign entienda y se pueda colocar en una plantilla previamente diseñada, ahorrandonos un montón del trabajo que requiriríamos si el documento fuse importado a InDesign desde MS Word.

Las convenciones para Markdown están disponibles en varios tipos o “flavors”, diseñados para su uso en contextos particulares como blogs, wikis o repositorios de código. El flavor de Markdown utilizado por Pandoc está orientado para un uso académico. Sus convenciones están descritas en la página de Pandoc’s Markdown. Estas convenciones incluyen el “YAML” block, que contiene una serie de metadatos muy útiles.

Vamos a crear ahora un documento en Markdown. Abre tu editor de texto plano seleccionado y escribe algo que debe tener un aspecto como el siguiente (o sencillamente corta y pega el texto):

```
---
title: Nuestro libro de prueba
author: Gabriel García
date: 27 de mayo de 2020
fontfamily: times
---
```

El Markdown “Pandoc-flavored” almacena cada uno de los valores anteriores y los “imprime” en la ubicación apropiada de tu documento de salida una vez que está listo para exportar. Más adelante aprenderemos a incluir campos más potentes en YAML. Por ahora, vamos a suponer que estamos escribiendo un libro compuesto por tres capítulos, cada una subdividida en dos apartados. Hay que dejar una línea en blanco después de los tres últimos guiones del bloque YAML para que puedas pegar lo que sigue:

```
# capítulo 1

## Sección 1

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
```

El siguiente párrafo debe empezar como éste, sin sangría:

```
## Sección 2

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque  ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.

# capítulo 2

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

## Sección1

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque  ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.
```

Sigue adelante e introduce cualquier texto de relleno. Los espacios vacíos tienen significado en Markdown por lo que no debes poner sangría en los párrafos pero sí es importante que separes los párrafos con una línea en blanco. Las líneas en blanco también deben preceder a los encabezados de sección.

Puedes añadir asteriscos para dar énfasis a las palabras con negritas o cursivas de esta manera: *cursivas* y **negritas**. También podemos añadir a nuestro texto un enlace y una nota a pie de página para cubrir los requisitos de un texto promedio. Escribe:

```
Una oración que requiere una cita.[^1]

[^1]: ¡Ésta es mi primer nota a pie de página! Y un [enlace](https://www.eff.org/).
Cuando el texto del enlace y la dirección del mismo son iguales es más rápido escribir: <https://www.eff.org/>, en vez de [https://www.eff.org/](https://www.eff.org/).
```
Vamos a guardar nuestro archivo antes de ir más lejos. Haz una carpeta para albergar este proyecto. Es probable que tengas un sistema de organización de tus documentos, proyectos, ilustraciones y bibliografías, pero a menudo tu documento, tus proyectos, tus ilustraciones y bibliografías se encuentran en diferentes carpetas, lo que los hace difíciles de encontrar. Nuestro objetivo es crear una carpeta única para cada proyecto con todos los materiales relevantes incluidos en ella. La regla general es “un proyecto, un texto, una carpeta”. Denomina a tu archivo algo así como “principal.md”, donde “md” significa que es un archivo Markdown.

Una vez que has guardado el archivo, vamos a añadir una imagen. Copia una imagen pequeña a la carpeta y añade lo siguiente en alguna parte del cuerpo de texto: ``![una imagen](tu_imagen.jpg).``

En este punto tu archivo principal.md debe verse como sigue:

```
---
title: Flujo de trabajo en texto plano
author: Gabriel García
date: 20 de enero de 2014
---

# Sección 1

## Subsección 1.1

Lorem *ipsum* dolor sit amet, **consectetur** adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

El siguiente párrafo debe empezar como este, sin sangría:

## Subsección 1.2

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque  ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.

# Sección 2

## Subsección 2.1
![una imagen](tu_imagen.jpg)

## Subsección 2.2.

Una oración que requiere una cita.[^1]

[^1]: ¡Ésta es mi primer nota a pie de página! Y un [enlace](https://www.eff.org/).
```

Y como veremos en breve, este archivo de texto plano se puede representar como un muy buen PDF.

Si quieres tener una idea de cómo serán interpretado en un fomato HTML este tipo de marcado, prueba este sitio de prueba en línea y juega con varios tipos de sintaxis. Recuerda que ciertos elementos del Pandoc-flavored markdown (como el bloque de título o las notas al pie) no funcionan en esta versión web ya que solamente acepta lo básico.

En este punto, deberás ocupar algún tiempo explorando algunas de las características de Markdown como las citas de texto (referidas con el símbolo >), los listados que empiezan con * o -, los saltos de línea literales que empiezan con | (útiles para poesía), las tablas y algunas otras funciones señaladas en la página sobre Markdown de Pandoc.

Presta particular atención a los espacios en blanco y al flujo de los párrafos. La documentación lo explica sucintamente cuando define un párrafo como “una o más líneas de texto seguidas por una o más líneas en blanco.” Considera que “las nuevas líneas son tratadas como espacios” y que “si necesitas un salto de línea elocuente, utiliza dos o más espacios en blanco al final de la línea.” La mejor manera de entender lo que significa es experimentar libremente. Utiliza el modo de vista previa de tu editor o solamente ejecuta Pandoc para ver los resultados de tus experimentos.

Pero sobre todo, evita la necesidad de formatear. Recuerda que estás identificando unidades semánticas: secciones, subsecciones, énfasis, notas al pie y figuras. Incluso *cursivas*y **negritas** en Markdown no son en realidad marcas de formato, sino que indican un nivel diferente de énfasis. La aplicación del formato sucederá después, una vez que conozcas el momento del proceso en el que hay que hacerlo y los requerimientos de la publicación.

Existen programas que te permiten obtener una vista previa en vivo de la salida de markdown al tiempo que editas tu archivo de texto plano y que detallaremos más adelante en la sección de Recursos útiles. Algunos de ellos soportan notas a pie, figuras, incluso bibliografías. Sin embargo, para sacar provecho al máximo de Pandoc, te recomendamos que te quedes con lo más sencillo: archivos de texto plano almacenados localmente en tu computadora.
