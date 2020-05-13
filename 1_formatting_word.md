# Modulo uno: preparar el archivo word para producción

El propósito de esta propuesta de flujo de trabajo es automatizar al máximo o lo que es equivalente, dejar que el software haga el trabajo por nosotros. Con esto en mente, nuestra tarea es ponerselo fácil y minimizar al máximo las posibilidades de error.

## Caso 1

Lo más común es que el archivo que pasemos a producción, una vez este halla sido editado y corregido, sea un archivo formateado en MS Word. ¿Que condiciones debe cumplicar este archivo para entrar en nuestro workflow?

### Estar estructurado semánticamente

En esta fase no nos debe importar en lo más mínimo el diseño, aquí se trata de estructurar el archivo correctamente para que luego pueda acoger nuestro diseño. Lo primero, entonces, es procurar que esté estructurado correctamente. Y esto es equivalente a prepara cuidadosamente el outline del libro.

  - asignar encabezados para estructurar el documento 
  - heading 1 para el título
  - heading 2 para los capítulos (o para las secciones, si es el caso, reservando el heading 3 para capítulos)
  - Un estilo para los bloques de texto (como las citas, por ejemplo)
  - Un estilo para las notas al pie de página
  - Revisar que el formateo local (itálicas y negritas) esté aplicado consistentemente

  Todo esto nos permitirá mapear correctamente los estilos generados al momento de importarlo en InDesign y en epub. En InDesign, el mapeo (pero lo veremos a continuación) se realizará a partir de una plantilla ya diseñada. Y en EPUB, a partir de una hoja de estilos.

En una novela cualquiera, pongamos por caso, Moby Dick, el outline sería algo así como: (pantallazo)

### Dificultades

Si utilizaramos unicamente una misma versión de word, todo esto sería en general bastante trivial. pero lo cierto es que la práctica indica que tenemos que lidiar con archivos formateados de forma muy diversa y en vesriones muy distintas de Word. Si es una versión antigua, podemos tener un archivo con la extensión .doc (el estandar antiguo de MS Word, en uso hasta 2003)

## Checklist

[ ] ¿Están los estilos asignados consistentemente?


- Limpiar el documento
  - fuera de los estilos estrictamente necesarios, no debería haber otros
  - no debería haber fuentes distintas en el texto
  - no deberían haber espacios en blanco (todo el espaciado del documento debería estar determinado en los estilos de indesign y en el css para los formatos web y epub)

La idea es eliminar al máximo todo lo que pueda ocasionar ruido innecesario. Word es un buen procesador de texto, pero [genera una cantidad sorprendente de código inutil](https://slate.com/technology/2012/04/microsoft-word-is-cumbersome-inefficient-and-obsolete-its-time-for-it-to-die.html)
, destinado principalmente a establecer como debe el texto a mostrase en una página impresa. Pero, dado que en esta fase nuestro target es crear un documento que esté orientado al mismo tiempo a pantallas y a impresión, toda esa información debería ser establecida en las plantillas que diseñemos para generar los distintos formatos de salida. 

## pasos

vamos a tomar un documento Word. Aparentemente está bien formateado. Si lo miramos, podemos comprobar que las marcas de corte están bien, que visualmente se marcan los títulos y subtítulos, que el texto tiene una tipo bonita y agradable. Y sin embargo.
Veamos mejor. Si aplicamos el inspector de estílos de word al texto, vemos que los subtítulos y el nombre del autor, están formateados en estilo de párrafo "normal". Se ve bien, claro, pero no sirve. Cuando coloquemos el texto en indesign (o lo convirtamos a markdown o HTML) ese formato se va a transformar en código impredecible y, lo más importante, no va a generar encabezados (pero esto lo veremos luego), que serán necesarios para dividir el libro en distintos archivos (para el formato epub), generar los índices (en indesign y epub) sin contar con que tendremos poco o ningun control sobre el diseño de estos encabezados. Y sin embargo, es tan fácil como asignarle un estilo correcto. No se ve tan bien como qusieramos, pero en esta fase, eso no es lo importante.
