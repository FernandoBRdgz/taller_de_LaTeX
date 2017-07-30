# Taller de Introducción a LaTeX

## TL21: Clases de documentos en LaTeX

---

**Objetivo:** En esta actividad aprenderás e identificarás:

* Las clases estándar de documentos en LaTeX.

* Algunas de las opciones básicas para las clases de documentos en LaTeX.

**Introducción:** En LaTeX los comandos que dan formato se identifican con facilidad, pues siempre comienzan con una diagonal invertida `\`.
En el editor TeXnicCenter, como en muchos otros, los comandos de LaTeX aparecen en color azul.

Por ejemplo, en la Actividad TL11: Primera prueba, aparece la primera línea

```latex
\documentclass{article}
```

que es el comando que indica a LaTeX la clase de documento que será compilado.

Las cinco clases para documentos estándar son los que se muestran en la Tabla 1.

| Clase      | Propósito                                               |
| ---------- | ------------------------------------------------------- |
| article    | Artículos para revistas científicas, tutoriales, etc.   |
| report     | Textos largos como tesis, reportes, etc.                | 
| book       | Libros o documentos con una estructura similar.         |
| letter     | Cartas.                                                 |
| slides     | Transparencias.                                         |

Así como puede establecerse la clase de documento que LaTeX compilará, también es posible adecuar el formato
de cada una de ellas por medio de las opciones expuestas en la Tabla 2.

| Opción de clase | Propósito                                                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| 11pt            | Especifica un tamaño de fuente de 11 puntos (10% más grande que el predefinido de 10 puntos.                                              |
| 12pt            | Especifica un tamaño de funtes de 12 puntos.                                                                                              | 
| twocolumn       | Produce un documento con dos columnas en cada página                                                                                      |
| twoside         | Produce un documento que será impreso por ambos lados, configurando automáticamente los encabezados y pies de página para este propósito. |
| a4paper         | Genera un documento que será impreso en hojas de tamaño A4.                                                                               |
| landscape       | Cambia la orientación de la impresión de vertical a horizontal.                                                                           |

Las opciones de clase deben escribirse entre corchetes `[ ]` para indicarle a LaTeX qué opciones deberá activar. Por ejemplo:

```latex
\documentclass[12pt,twocolumn]{article}
```

Donde se especifica que se desea crear un documento del tipo artículo a dos columnas con fuente de 12 puntos.

Dependiendo de símbolos, gráficos, idiomas y colores, entre otros, que se deseen utilizar para elaborar un documento se
debe indicar que se hará uso de "paquetes” que contienen comandos para este propósito.
Los paquetes a usar se declaran en el preámbulo del documento (entre los comandos `\documentclass{}` y `\begin{document}`).

Por ejemplo,

```latex
\documentclass[12pt,twocolumn]{article}
\usepackage[spanish]{babel}
\usepackage[utf8]{inputenc}
```

indica que se desea crear un documento del tipo artículo a dos columnas con fuente de 12 puntos en el idioma español.

La última instrucción se usa para facilitar el uso de acentos en LaTeX. Normalmente, un acento en LaTeX se indica con `\'` seguido
de la letra sobre la que se desea poner el acento:

`Ra\'ul`

Por supuesto, el indicar así cada acento en nuestro documento podría volverse impráctico, por lo que se sugiere ampliamente el uso del paquete
`inputenc` con la opción `utf8` para escribir acentos con facilidad.

Por otra parte, la opción `spanish` es útil para indicar que la separación de palabras deberá seguir las reglas gramaticales propias de español
(por ejemplo, que se separará en caso de ser necesario la palabra "redacción" como re-dac-ción y no como re-dac-ci-ón).

Para terminar esta breve reseña, cabe destacar dos aspectos:

* El título y el autor del documento se especifican por medio de las instrucciones 

```latex
\title{Título del documento}
\author{Nombre del autor}
```

* La fecha en que el documento fue escrito se especifica a través de la instrucción 

```latex
\date{fecha}
```

Estas tres instrucciones deben escribirse en el preámbulo del documento; y la instrucción 

```latex
\maketitle
```

en el cuerpo del mismo (de otro modo esta información no aparecerá en el documento). 

Todo aquello que se escriba después del comando `\end{document}` será interpretado por LaTeX como comentarios que no deben ser compilados;
dentro del cuerpo del documento (todo lo que aparece entre los comandos `\begin{document}` y `\end{document}`)pueden precisarse comentarios
siempre que sean antecedidos por el símbolo `%` apareciendo en color gris: 

```latex
%Esto es un comentario.
```


I. Ahora que conoces algunas clases básicas, y algunas de sus opciones, copia y pega el siguiente texto:

Una de las principales problemáticas de nuestro tiempo es la creciente complejidad de la estructura y funcionamiento de sistemas modernos, por lo que se requiere de nuevos métodos formales apropiados para la especificación de sistemas y para su validación tanto cualitativa como cuantitativa. Las redes de Petrison formalismos útiles en el análisis de sistemas modernos ya que permiten describirlos de manera concisa y apropiada debido a que ofrecen una representación gráfica ordenada, versátil y lógica de los módulos que componen a un sistema, así como de la interacción que guardan éstos entre sí. Las redes de Petri fueron creadas en 1962 por Carl Adam Petri para su tesis doctoral, en la cual describe sus fundamentos teóricos. Desde entonces, cada vez son más los estudiosos de este tema y han surgido muchas variedades de las mismas en los últimos años.

Cuando la aleatoriedad se manifiesta en un sistema la complejidad del mismo aumenta considerablemente, por lo que es necesario el uso de herramientas probabilísticas que permitan su correcta modelación y estudio. La teoría de la probabilidad se inició prácticamente con el análisis matemático de los juegos de azar realizado primero por los matemáticos Pierre du Fermat (1601-1665) y Blas Pascal (1623-1662). Christian Huygens (1629-1695) publicó en 1657 el primer tratado sobre problemas relacionados con juegos de azar, el cual sirvió como base para el gran desarrollo experimentado por esta teoría durante el siglo XVIII, con el aporte de Jacobo Bernoulli (1654-1705) y Pierre Simon Laplace (1749-1827). Fueron Markov (1856-1922) y Kolmogorov (1903-1987) dos de los principales matemáticos que contribuyeron al estudio de la aleatoriedad a través de modelos conocidos como procesos estocásticos, los cuales permiten modelar una amplia gama de fenómenos, bajo un sólido fundamento matemático.

II. Genera un documento empleando una clase adecuada para textos largos, con fuente de 12 puntos, en español.

III. Guarda el archivo y compílalo para generar un PDF.
