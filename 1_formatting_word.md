# Modulo uno: preparar el archivo word para producción

Supongamos que tenemos el documento final, ya corregido y editado y listo para entrar en producción, ¿Qué necesitamos comprobar?

## Checklist

[ ] ¿Están los estilos asignados consistentemente?

Esto supone:
- asignar encabezados para estructurar el documento 
  - heading 1 para el título, 
  - heading 2 para los capítulos, 
  - Un estilo para los bloques de texto (como las citas, por ejemplo), 
  - Un estilo para las notas al pie de página
  - Revisar que el formateo local (itálicas y negritas) esté marcado consistentemente
- Limpiar el documento
  - fuera de los estilos estrictamente necesarios, no debería haber otros
  - no debería haber fuentes distintas en el texto
  - no deberían haber espacios en blanco (todo el espaciado del documento debería estar determinado en los estilos de indesign y en el css para los formatos web y epub)

La idea es eliminar al máximo todo lo que pueda ocasionar ruido innecesario. Word es un buen procesador de texto, pero genera una cantidad sorprenente de código inutil, destinado principalmente a establecer como debe el texto a mostrase en una página impresa. Pero, dado que en esta fase nuestro target es crear un documento que esté orientado al mismo tiempo a pantallas y a impresión, toda esa información debería ser establecida en las plantillas que diseñemos para generar los distintos formatos de salida. 
esta es una nueva edición

## 


