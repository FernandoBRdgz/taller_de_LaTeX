# Taller de Introducci�n a LaTeX

## TL21: Clases de documentos en LaTeX

**Objetivo:** En esta actividad aprender�s e identificar�s:

* Las clases est�ndar de documentos en LaTeX.

* Algunas de las opciones b�sicas para las clases de documentos en LaTeX.

**Introducci�n:** En LaTeX los comandos que dan formato se identifican con facilidad, pues siempre comienzan con una diagonal invertida ( \ ).
En el editor TeXnicCenter, como en muchos otros, los comandos de LaTeX aparecen en color azul.

Por ejemplo, en la Actividad TL11: Primera prueba, aparece la primera l�nea

```latex
\documentclass{article}
```

que es el comando que indica a LaTeX la clase de documento que ser� compilado.

Las cinco clases para documentos est�ndar son los que se muestran en la Tabla 1.

| Clase      | Prop�sito                                               |
| ---------- | ------------------------------------------------------- |
| article    | Art�culos para revistas cient�ficas, tutoriales, etc.   |
| report     | Textos largos como tesis, reportes, etc.                | 
| book       | Libros o documentos con una estructura similar.         |
| letter     | Cartas.                                                 |
| slides     | Transparencias.                                         |

As� como puede establecerse la clase de documento que LaTeX compilar�, tambi�n es posible adecuar el formato
de cada una de ellas por medio de las opciones expuestas en la Tabla 2.

| Opci�n de clase | Prop�sito                                                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| 11pt            | Especifica un tama�o de fuente de 11 puntos (10% m�s grande que el predefinido de 10 puntos.                                              |
| 12pt            | Especifica un tama�o de funtes de 12 puntos.                                                                                              | 
| twocolumn       | Produce un documento con dos columnas en cada p�gina                                                                                      |
| twoside         | Produce un documento que ser� impreso por ambos lados, configurando autom�ticamente los encabezados y pies de p�gina para este prop�sito. |
| a4paper         | Genera un documento que ser� impreso en hojas de tama�o A4.                                                                               |
| landscape       | Cambia la orientaci�n de la impresi�n de vertical a horizontal.                                                                           |

Las opciones de clase deben escribirse entre corchetes `[ ]` para indicarle a LaTeX qu� opciones deber� activar. Por ejemplo:

```latex
\documentclass[12pt,twocolumn]{article}
```

Donde se especifica que se desea crear un documento del tipo art�culo a dos columnas con fuente de 12 puntos.

Dependiendo de s�mbolos, gr�ficos, idiomas y colores, entre otros, que se deseen utilizar para elaborar un documento se
debe indicar que se har� uso de "paquetes� que contienen comandos para este prop�sito.
Los paquetes a usar se declaran en el pre�mbulo del documento (entre los comandos `\documentclass{}` y `\begin{document}`).

Por ejemplo,

```latex
\documentclass[12pt,twocolumn]{article}
\usepackage[spanish]{babel}
\usepackage[utf8]{inputenc}
```

indica que se desea crear un documento del tipo art�culo a dos columnas con fuente de 12 puntos en el idioma espa�ol.

La �ltima instrucci�n se usa para facilitar el uso de acentos en LaTeX. Normalmente, un acento en LaTeX se indica con `\'` seguido
de la letra sobre la que se desea poner el acento:

`Ra\'ul`

Por supuesto, el indicar as� cada acento en nuestro documento podr�a volverse impr�ctico, por lo que se sugiere ampliamente el uso del paquete
`inputenc` con la opci�n `utf8` para escribir acentos con facilidad.

Por otra parte, la opci�n `spanish` es �til para indicar que la separaci�n de palabras deber� seguir las reglas gramaticales propias de espa�ol
(por ejemplo, que se separar� en caso de ser necesario la palabra "redacci�n" como re-dac-ci�n y no como re-dac-ci-�n).

Para terminar esta breve rese�a, cabe destacar dos aspectos:

* El t�tulo y el autor del documento se especifican por medio de las instrucciones 

```latex
\title{T�tulo del documento}
\author{Nombre del autor}
```

* La fecha en que el documento fue escrito se especifica a trav�s de la instrucci�n 

```latex
\date{fecha}
```

Estas tres instrucciones deben escribirse en el pre�mbulo del documento; y la instrucci�n 

```latex
\maketitle
```

en el cuerpo del mismo (de otro modo esta informaci�n no aparecer� en el documento). 

Todo aquello que se escriba despu�s del comando `\end{document}` ser� interpretado por LaTeX como comentarios que no deben ser compilados;
dentro del cuerpo del documento (todo lo que aparece entre los comandos `\begin{document}` y `\end{document}`)pueden precisarse comentarios
siempre que sean antecedidos por el s�mbolo `%` apareciendo en color gris: 

```latex
%Esto es un comentario.
```


I. Ahora que conoces algunas clases b�sicas, y algunas de sus opciones, copia y pega el siguiente texto:

Una de las principales problem�ticas de nuestro tiempo es la creciente complejidad de la estructura y funcionamiento de sistemas modernos, por lo que
se requiere de nuevos m�todos formales apropiados para la especificaci�n de sistemas y para su validaci�n tanto cualitativa como cuantitativa.
Las redes de Petrison formalismos �tiles en el an�lisis de sistemas modernos ya que permiten describirlos de manera concisa y apropiada debido a que ofrecen
una representaci�n gr�fica ordenada, vers�til y l�gica de los m�dulos que componen a un sistema, as� como de la interacci�n que guardan �stos entre s�.
Las redes de Petri fueron creadas en 1962 por Carl Adam Petri para su tesis doctoral, en la cual describe sus fundamentos te�ricos. Desde entonces,
cada vez son m�s los estudiosos de este tema y han surgido muchas variedades de las mismas en los �ltimos a�os.

Cuando la aleatoriedad se manifiesta en un sistema la complejidad del mismo aumenta considerablemente, por lo que es necesario el uso de herramientas
probabil�sticas que permitan su correcta modelaci�n y estudio. La teor�a de la probabilidad se inici� pr�cticamente con el an�lisis matem�tico de los
juegos de azar realizado primero por los matem�ticos Pierre du Fermat (1601-1665) y Blas Pascal (1623-1662). Christian Huygens (1629-1695) public� en
1657 el primer tratado sobre problemas relacionados con juegos de azar, el cual sirvi� como base para el gran desarrollo experimentado por esta teor�a
durante el siglo XVIII, con el aporte de Jacobo Bernoulli (1654-1705) y Pierre Simon Laplace (1749-1827). Fueron Markov (1856-1922) y Kolmogorov (1903-1987)
dos de los principales matem�ticos que contribuyeron al estudio de la aleatoriedad a trav�s de modelos conocidos como procesos estoc�sticos, los cuales
permiten modelar una amplia gama de fen�menos, bajo un s�lido fundamento matem�tico.

II. Genera un documento empleando una clase adecuada para textos largos, con fuente de 12 puntos, en espa�ol.

III. Guarda el archivo y comp�lalo para generar un PDF.
