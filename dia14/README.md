# Unidades de Medidas en CSS: px, %, em, rem

## Pixel

Unidad absoluta minima que representa un punto en la pantalla. Son ideales para tamaños y dimensiones que no deben cambiar en relacion con otros elementos. Es recomendable usarlo para bordes imagenes y otros elementos de dimensiones fijas.

## Porcentaje

Es una relativa al tamano del elemento padre. Ej: el padre es de 200px y el elemento tiene un width de 50%, el ancho sera de 100px. Esta medida es util para diseños fluidos y responsive que se adapten al tamaño de pantalla. Es recomendable para contenedores que varien segun el contenedor.

## EM "em"

La unidad EM es relativa al tamaño de la fuente del elemento padre (o el suyo). Por ejemplo si el padre tiene un font-size: 10px y un marfin: 3 em; el margen sera de 30px. Esta unidad es buena para crear tamaños que escalen con el tamaño de la fuente. 

## REM

Es relativa al tamaño de la fuente de la RAIZ del documento. Por ejemplo si el tamaño de la fuente del HTML es de 8px y un elemento descendente en varios niveles tiene una medida de 3rem su medida sera de 24 px Rem es util para mantener una escala consistente en todo el documento independientemente de la estrucutra del DOM. 