---
layout: post
title: "Resumen de Clean Code - primera parte"
date: 2009-09-21 12:00
comments: true
categories: good practics
---

Ultimamente he estado leyendo Clean Code, el ultimo libro del para mi gusto genial Robert Martin. El libro, como el titulo indica :P, esta orientado a proporcionar un conjunto de buenas practicas y recomendaciones para escribir mejor código, código más limpio y más legible.

El libro no se queda sólo en decir "hazlo así que si no esta mal" sino que presenta ejemplos bastante exahustivos de refactorización de código existente (por ejemplo refactorizado una clase del framework JUnit), digamos que el libro esta dividido en 3 partes:

Capitulos teoricos, donde se exponen y justifican las buenas practicas recomendadas
Capitulos practicos, donde se coje un código existente y se intenta mejorar aplicando las buenas practicas expuestas en los capitulos teoricos
Un resumen de las buenas practicas en forma de "smells" y heuristicas simples. No esta mal como pequeña guia en plan recordatorio, siempre y cuando te hayas leido el resto del libro claro, por si solo no es demasiado útil.
Los capitulos teoricos van del 1 al 13, os cuento que es lo que más me ha gustado/llamado la atención en estos capitulos, el resto simplemente hay que leerselos, no tiene mucho sentido hacer un resumen de las partes practicas.

Capitulo 1 - Clean Code

Es un capitulo introductorio para justificar la intención del libro, recoje las opiniones de personalidades importantes de esto del desarrollo de software resaltando la importancia de escribir buen código, gente como Bjarne Stroustrup, Michael Feathers, Ron Jeffries o Grady Booch.

La idea principal del capitulo es que no hay nada más importante que escribir código de calidad para el exito de un proyecto, el autor utiliza muy a menudo la palabra "profesionalidad", hace mucho enfasis en dejar claro que un profesional responsable debe escribir siempre buen código, sean cuales sean las circunstancias, tiempos ajustados por ejemplo, ya que no hay nada que retrase más un proyecto que precisamente el mal código, tenemos que ser profesionales de verdad y hacer lo mejor que sepamos para garantizar la calidad de nuestro trabajo, en resumen, no ser chapuceros, que cada vez que hacemos una chapuza muere un gatito! :P

Me encanta de este capitulo que se de al código la importancia que tiene, algo obvio para cualquier desarrollador responsable, pero parece que no tan obvio para la gran mayoría del espectro de empresas que desarrollan software en esta nuestra querida españa :P (es el ambito que conozco, pero no creo que sea muy diferente en otras partes). Basta ya de adjetivos peyorativos como "picateclas", basta ya de menosprecioar la actividad más importante en el desarrollo de software: PROGRAMAR. Cuando esto se entienda, cuando las cosas se pongan en su lugar y se valore a los buenos profesionales que saben escribir clean code, entonces lo mismo empieza a cambiar un poquito esta industria.

Capitulo 2 - Meaningful Names

Pues si, un capitulo enterito para decir que escribamos nombres significativos para variables, funciones, clases etc,etc. Pero es que hay pocas cosas más determinantes para que un código sea legible como que tenga nombres en condiciones, pocas cosas más horribles que encontrase con variables tipo "aux1, aux2" o paquetes nombrados como "GUSU" en lugar de "my.company.servicios.gestion.usuarios" (ejemplo real :P )

Algunas recomendaciones que se ofrecen en el libro: usar verbos para nombrar los metodos y sustantivos para las clases, utilizar nombres pronunciables (esta me encanta, el código se LEE, si no puedo pronunciarlo me cuesta más esfuerzo leerlo), no usar notaciones tipo "los enteros empiezan por i, las cadenas por s" y chorradas similares (luego alguien cambia el tipo y se olvida de refactorizar el nombre... también tengo casos reales de esto :P ), no ahorrar caracteres poniendo abreviaturas, por ejemplo escribir "valEdadCli(...)" en lugar de "validarEdadDeCliente(...)".

Capitulo 3 - Functions

El capitulo trata de como escribir buenas funciones/metodos, la recomendación más importante del autor en este punto es sencilla: escribe funciones pequeñas. Si luego mirais las refactorizaciones de ejemplo en los capitulos practicos no encontrareis funciones de más de 10 o 20 lineas como muchisimo, totalmente de acuerdo con esta afirmación, sobre todo con lo facil que es refactorizar con cualquier IDE actual, no tiene disculpa escribir funciones de 100 o 200 lineas como se ven por ahí, no es muy profesional que digamos...

Otra recomendación importante es sobre el número de parametros que recibe una función, para el autor 3 parametros es el limite antes de empezar a pensar que algo estamos haciendo mal.

Capitulo 4 - Coments

Este capitulo personalmente me encanta, porque en el pasado me ha tocado discutir bastante por defender algunas de las cosas que precisamente defiende el tio bob en este libro, y ahora cuanto me toque discutir otra vez por lo menos tengo una buena referencia jeje.

Particularmente lo que más me gusta es una idea que creo que no todo el mundo tiene clara respecto a los comentarios, la gente considera a los comentarios como algo bueno, al código comentado como algo bueno: "mira que bien, esta todo comentado". El tio bob lo enfoca de otro modo, dice algo como "cada vez que escribes un comentario estas fallando como programador, tienes que escribir un comentario para clarificar algo porque no has sabido utilizar las herramientas que tienes (el lenguaje de programación) para dejar claras tus intenciones". Es decir, poner un comentario es el el ultimo recurso cuando despues de darle muchas vueltas no se te ocurre como clarificar una parte del código, en lugar de dedicar tiempo a escribir comentarios, dedicalo a arreglar tu código para que se entienda sin la necesidad de estos. No te olvides que estas usando un lenguaje de programación, aprende a usarlo correctamente y no ocultes tus carencias con este lenguaje añadiendo notitas al lado en otro lenguaje que dominas mejor y en el que si puedes expresarte (aunque bueno... esto no siempre es así tampoco que se ve cada comentario xd)

Otras recomendaciones son no escribir comentarios redundantes (tipica función "getEdad()" que tiene como comentario "devuelve la edad" ¿en serio?, que sorpresa!), otra que me gusta mucho: "el código comentado es una abominación, borralo!", odio y lo digo muy en serio, odio, el código comentado, si no lo vas a usar borralo que para volver atras tienes el sistema de control de versiones (y si no sabes usarlo, aprende, pero no enguarrines el código!). Una variante de esto ultimo en C/C++ muy divertida con la que me he encontrado alguna vez es usar bloques tipo "#ifdef 1/0", es muy divertido porque el editor como es lógico no muestra el contenido de un bloque "ifdef" que nunca se va a ejecutar de una forma especial, con lo que te puede llevar un buen rato descubrir que llevas media hora tratando de entender un trozo de código que jamas se ejecuta...

Con esto termino de momento que me esta quedando muy largo, en un proximo post termino de contar el resto de capitulos del libro.