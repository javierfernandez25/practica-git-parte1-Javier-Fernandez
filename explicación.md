Creé una rama nueva para provocar el conflicto
Partí desde main y abrí una rama llamada feature-conflicto. La idea era tener dos líneas de trabajo distintas que tocasen la misma línea del mismo archivo.

Modifiqué la misma línea en cada rama con contenidos diferentes

En feature-conflicto edité la primera línea de notas.md y guardé esos cambios.

Volví a main y edité esa misma primera línea, pero con un texto distinto.
Así me aseguré de que, al intentar juntar las ramas, Git detectara que no sabía cuál versión elegir.

Intenté fusionar (merge) feature-conflicto dentro de main
Al hacerlo, Git dijo: “oye, en notas.md hay un conflicto”. Entonces marcó el archivo con unas etiquetas especiales para que yo decidiera:

<<<<<<< HEAD → lo que tiene ahora main

======= → separador

>>>>>>> feature-conflicto → lo que viene de la otra rama

Resolví el conflicto a mano
Abrí notas.md, leí ambas versiones y decidí qué dejar (por ejemplo, una versión combinada).
Borré los marcadores (<<<<<<<, =======, >>>>>>>) y dejé solo el texto final que quería mantener. Guardé.

Le dije a Git “ya está resuelto” y cerré la fusión
Añadí el archivo modificado y confirmé el “merge”. Con eso, main quedó actualizado con la resolución del conflicto.

Documenté lo que hice
Creé un archivo conflicto.md donde expliqué qué líneas chocaban, qué versiones había y qué decisión tomé para resolverlo.

Subí los resultados a GitHub
Envié los cambios de main al remoto para que todo quedara también reflejado en GitHub.
(Y, si la rama feature-conflicto ya no hacía falta, se podía borrar).
