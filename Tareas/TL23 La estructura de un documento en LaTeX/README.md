# Taller de Introducción a LaTeX

## TL23:La estructura de un documento en LaTeX

---

**Objetivo:** En esta actividad reconocerás la estructura básica de un documento elaborado con LaTeX e identificarás las funciones específicas de algunos comandos esenciales de formato.

**Introducción:** 

* Partes de un documento

Las clases `{book}`, `{article}` y `{report}` permiten estructurar los documentos en capítulos, secciones y subsecciones; con los comandos

```latex
\chapter{Nombre de capítulo} 
\section{Nombre de sección} 
\subsection{Nombre de subsección}
```

Estos comandos son de gran utilidad, pues permiten la creación automática del índice a través de la instrucción `\tableofcontents` en el cuerpo del documento... ¡LaTeX se encarga de la numeración automática de estos elementos y de la actualización de las páginas a la que corresponden! Es conveniente "correr” por lo menos dos veces el archivo para que la actualización surta efecto.

También es posible dividir en partes un documento extenso a través del comando 

```latex
\part{nombre de la parte}
```

o incluir un resumen con 

```latex
\abstract{Texto del resumen}
```

* Portada de un documento

Para crear la portada de un documento de LaTeX basta con escribir el comando `\maketitle` en el cuerpo del documento y en el preámbulo del documento los comandos ya vistos: 

```latex
\title{Título del documento}
\author{Nombre del autor}
\date{Fecha} %Si se deja sin ningún argumento se actualizará automáticamente la fecha.
```

* Referencias cruzadas 

También pueden crearse referencias cruzadas a lo largo del documento. Esto es posible a través de los comandos

```latex
\label{sec:etiqueta}
\ref{sec:etiqueta}
```

La ventaja de usar estos comandos radica en que no importa si se añaden o eliminan secciones precedentes, LaTeX actualizará la referenciación. El siguiente ejemplo muestra el resultado arrojado por estos comandos:

**Ejemplo**

```latex
\section{¿Cómo hacer referencias cruzadas?}
\label{sec:refcruz}
\subsection{Creación de etiquetas}
Las referencias cruzadas en $\LaTeX$ son sencillas de elaborar. Primero, es necesario crear una etiqueta. El nombre de la etiqueta de la sección \emph{¿Cómo hacer referencias cruzadas?} es refcruz.
\subsection{Referencia a una etiqueta}
Una vez definida una etiqueta, puede hacerse referencia a ella. Por ejemplo:
\emph{La sección \ref{sec:refcruz} muestra cómo elaborar referencias cruzadas}.
```

* Pies de página 

Los pies de página se incluyen con la instrucción:

```latex
\footnote{Texto del pie de página}
```

**Ejemplo**

Este texto se encuentra en el cuerpo del documento.`\footnote{Este es un pie de página.}`

* Listas numeradas y viñetas

Las listas numeradas y las viñetas pueden crearse a partir de los entornos `{enumerate}` e `{itemize}` respectivamente.  A continuación, algunos ejemplos:

**Ejemplos**

```latex
\begin{enumerate}
\item Un elemento.
\item Otro elemento.
\end{enumerate} 
```

```latex
\begin{itemize}
\item Un elemento.
\item Otro elemento.
\end{itemize}
```

```latex
\begin{description}
\item [(i)] Un elemento.
\item [(ii)]Otro elemento.
\end{description}
```

También pueden emplearse en forma anidada:

**Ejemplo**

```latex
\begin{enumerate}
\item Un elemento.
\begin{itemize}
\item Un elemento subordinado.
\item Otro elemento subordinado.
\end{itemize}
\item Otro elemento.
\end{enumerate}
```

* Tipos y tamaños de fuente

Existen muchos comandos para modificar la tipografía de la fuente. Los más comunes son los siguientes:

**Ejemplos**

Fuente estándar

```latex
\emph{emphasise}
\emph{abcdefghijklmnopqrstuvwxyz}
\emph{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

```latex
\textbf{bold}
\textbf{abcdefghijklmnopqrstuvwxyz}
\textbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

```latex
\textit{italic}
\textit{abcdefghijklmnopqrstuvwxyz}
\textit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

```latex
\textsl{slanted}
\textsl{abcdefghijklmnopqrstuvwxyz}
\textsl{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

```latex
\texttt{typewriter}
\texttt{abcdefghijklmnopqrstuvwxyz}
\texttt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

```latex
\textsc{small caps}
\textsc{abcdefghijklmnopqrstuvwxyz}
\textsc{ABCDEFGHIJKLMNOPQRSTUVWXYZ}
```

El tamaño de la fuente se establece por medio de los comandos `\tiny`, `\scriptsize`, `\footnotesize`, `\small`, `\normalsize`, `\large`, `\Large`, `\LARGE`, `\huge` o `\Huge` según el tamaño deseado:

* Justificación del párrafo

Los párrafos se justifican por medio de los entornos `{center}`, `{flushleft}` y `{flushright}`:

**Ejemplo**

```latex
\begin{center}
Texto\\ centrado
\end{center}
```

```latex
\begin{flushleft}
Texto\\ a la izquierda
\end{flushleft}
```

```latex
\begin{flushright}
Texto\\ a la derecha
\end{flushright}
```

Overleaf cuenta con la opción `More` dentro de la barra de herramientas que ayuda a introducir algunos de estos comandos.

**Descripcion:**

I. Elabora un documento de la clase artículo con: 

a. Portada (con título, autor y fecha). 
b. Resumen. 
c. Indice. 
d. Tres secciones. 
e. Al menos una referencia cruzada. 
f. Una lista numerada. 
g. Una lista con viñetas. 
h. Cinco tipos diferentes de fuente a lo largo del texto. 
i. Cinco tamaños distintos de fuente a lo largo del texto. 
j. Un párrafo centrado, uno alineado a la izquierda y otro a la derecha. 


