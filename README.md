¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD 1
El comando para movernos entre commits es "git reset". 
Con el indicador "--hard" le indicamos que queremos eliminar los cambios del working area.
Con "head~1" indicamos que queremos mover el puntero head al commit anterior del actual,
lo que "deshará" el último commit.

¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reset --hard 25e9bca
El comando para movernos entre commits es "git reset". 
Con el indicador "--hard" le indicamos que queremos eliminar los cambios del working area.
Con el código "25e9bca" identifca el commit al que queremos mover el puntero head, lo que deshace el último commit.

El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No, Cuando se crea la rama styled, el puntero head de master y styled apuntan al mismo nodo en el grafo. 
Luego se modifica el fichero git-nuestro.md en la rama styled y al hacer commit, genera un nuevo nodo 

El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si, Porque hemos el contenido del mismo fichero en dos ramas diferentes es distinto y git necesita 
aclarar cuál será el contenido bueno para el fichero al unir las dos ramas. 
Es necesario crear un nuevo nodo en el que converjan ambas ramas, haciendo un merge "no fast forward". 
En el nuevo nodo es dónde la versión final del fichero en conflicto debe ser considerado.

El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No porque esas dos ramas forman una lista.
Lo que hay que hacer es mover el puntero head de la rama master al mismo nodo al que apunta el puntero head de la rama styled.

¿Qué comando o comandos utilizaste en el paso 25?
git log --graph --decorate --pretty=oneline

El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si podría ser fast-forward porque el último commit del master y el último commit de title forman una lista y
al hacer un merge fast-forward el puntero head de master pasara a apuntar al commit donde apunta el puntero head de title.
Como master absorve a title solo necesita incluir los nodos que le falten de title.
Si forzamos el merge no fast forward obtenemos obligatoriamente un nuevo nodo en el que converjen ambas ramas.

¿Qué comando o comandos utilizaste en el paso 27?
git reset 6756b98
La etiqueta 6756b98 corresponde al commit donde se añade el título al fichero git-nuestro.md

¿Qué comando o comandos utilizaste en el paso 28?
git checkout git-nuestro.md

¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title

¿Qué comando o comandos utilizaste en el paso 30?
git reset --hard b82c866

¿Qué comando o comandos usaste en el paso 32?
git reset f60f285

¿Qué comando o comandos usaste en el punto 33?
git reset --hard cd4941f
