---
layout: default
title: "Minion 2: puzzle game"
parent: Trabajos Prácticos
---

## Trabajo Práctico Grupal “Minion 2”

En este TP vamos a trabajar game design y level design.
Se debe implementar un juego top-down de tipo puzzle en Godot, organizado sobre una grilla. Teniendo como referencia [Sokoban](https://en.wikipedia.org/wiki/Sokoban), [Fidel Dungeon Rescue](https://store.steampowered.com/app/573170/Fidel_Dungeon_Rescue/), [Baba is you](https://store.steampowered.com/app/736260/Baba_Is_You/), [A Good Snowman Is Hard To Build](https://store.steampowered.com/app/316610/A_Good_Snowman_Is_Hard_To_Build/), entre otros. También son interesantes como referencia algunos juegos de la [GMTK Game Jam 2019](https://www.youtube.com/watch?v=o-WrQ77zUvA).

Este tipo de puzzle games tienen dos características que nos interesan: es sencillo identificar las mecánicas que utilizan y los niveles son acotados, siendo más fáciles de analizar que en otros géneros.

Se recomienda utilizar [PuzzleScript](https://www.puzzlescript.net/) para prototipar y explicar ideas a sus compañeros, pero no es obligatorio.


### Nomenclatura:

 - Player: Representación controlada por el jugador.
 - Ítems: objetos que el jugador puede tomar del piso, equipar o soltar. No puede equipar más de un ítem a la vez.
 - Celda: espacio físico que conforma la grilla del mundo del juego. Una celda puede tener propiedades especiales. En una celda no puede haber más de un objeto al mismo tiempo (para este límite no se tiene en cuenta al player).
 - Bloque: objeto que ocupa espacio en una celda. Puede ser una caja, un enemigo, una pared, etc. Si lo desean, puede haber objetos que se comporten como ítems y bloques al mismo tiempo.


### Mecánicas

 Elegir entre 2 y 4 mecánicas de las siguientes opciones (y no más):
  - Player empuja bloques.
  - Player tiene cantidad de movimientos limitados. Por ejemplo, puede perder vida o combustible cada vez que avanza, y puede tomar ítems del piso para recargarse.
  - Player tiene una cantidad de tiempo limitado. Por ejemplo: celdas que se destruyen o se vuelven inhabitables; aumenta la cantidad de obstáculos; disminuye la vida del Player; items o recursos desaparecen; contadores. El tiempo restante puede verse afectado por otras mecánicas.
  - Bloques o celdas que causan daño (ej: lasser, un precipicio que se abre, muro de llamas, picas desde el piso, etc.). Cómo se modela ese daño depende de la implementación.
  - Una celda o elemento actúa como interruptor que activa otro elemento o celda. Puede ser un botón en el piso que reacciona a pressión, un detector de cercanía, de daño, de luz, etc. Activar puede implicar resumir un comportamiento pausado, cambiar el tipo de bloque o celda afectada, etc.
  - El Player tiene un ítem que le permite moverse en una dirección. Solamente puede moverse en la dirección indicada por el ítem. Se puede tomar un ítem del suelo pero eso implica dejar en el suelo el ítem que se tenía.
  - Luz y sombra. Solo pueden verse aquellas celdas que estén siendo iluminadas (implica que hay celdas u objetos que producen luz).
  - Bloques generadores, consumidores y de transporte. Por ejemplo, cables de electricidad, tubos de agua, prismas que controlan luz.
  - Bloque que se mueve hacia cierto estímulo. Por ejemplo es atraído por la luz, por el personaje, por algún tipo de bloque en particular, etc.
  - Cambia la manera de interactuar con un bloque según el ítem que se tenga equipado. Por ejemplo, solamente pueden empujarse bloques si se tiene cierto ítem, ídem con atravezar bloques, o incluso destruirlos o cambiar su tipo.


La idea es que las mecánicas que elijan sean implementadas de manera que resulten cohesivas. **Elegir más mecánicas no hace que el TP sea mejor, es más importante que estén bien implementadas.**

### Dinámicas

La manera en que el jugador interactúa con el mundo y controla al elemento Player queda a libre implementación, pero debe ser consistente con las mecánicas elegidas.


### Niveles

Armar al menos 3 niveles que no tengan más de 8x8 celdas aplicando las mecánicas elegidas, al menos dos niveles tienen que tener dos mecánicas o más. A la hora de construir un nivel, unicamente coloquen elementos que cumplan una función. Si ese elemento solamente está "de relleno", es mejor no ponerlo.


### Arte

Es suficiente con utilizar componentes simbólicos para representar los elementos del juego, alcanza con que los elementos sean legibles.


### Videos útiles

 - [Un análisis de level design](https://www.youtube.com/watch?v=UwBl7Rnkt78)
 - [Video sobre cómo Johnatan Blow construye puzzles](https://www.youtube.com/watch?v=2zK8ItePe3Y)
 - [What makes a good puzzle?](https://www.youtube.com/watch?v=zsjC6fa_YBg)
 - [Level design workshop: Solving Puzzle Design](https://www.youtube.com/watch?v=0xBJwrm9C8w)