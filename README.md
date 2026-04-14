# PROMO-67---EQUIPO-1---PROYECTO-MODULO-1

## Trivial de geografía

Pequeño juego interactivo en Python basado en preguntas de geografía. El objetivo es responder correctamente a una serie de preguntas hasta alcanzar la victoria… o evitar la derrota.

### Objetivo del juego

El jugador debe:

✅ Conseguir 5 respuestas correctas para ganar
❌ Evitar acumular 3 respuestas incorrectas, lo que supone perder

El juego finaliza automáticamente cuando se cumple una de estas condiciones.

### ¿Cómo funciona?

1. Las preguntas y respuestas se almacenan en un diccionario.
2. Se convierten en una lista y se mezclan aleatoriamente ```random.shuffle```.
3. El juego recorre las preguntas una a una con un blucle ```for ```:
    - Muestra la pregunta
    - Recoge la respuesta del usuario ```input()```
    - Compara con la respuesta correcta
    - Se actualizan los contadores de:
        ✅ aciertos
        ❌ fallos

4. Tras cada pregunta, se comprueba:
    - Si ha ganado
    - Si ha perdido
    - O si el juego continúa

Para mejorar la experiencia del usuario: hemos eliminado espacios innecesarios ```strip()``` e ignoramos mayúsculas y minúsculas ```lower()```. 
**Las tildes sí deberan ponerse correctamente**

### Decisiones de diseño
Durante el desarrollo del proyecto se tomaron varias decisiones para simplificar la lógica del juego y hacerlo más funcional.

En primer lugar, aunque inicialmente se intentó controlar el flujo del juego mediante un bucle ```while```, finalmente se optó por utilizar un bucle ```for``` para recorrer las preguntas. Esta decisión permitió organizar mejor la lógica del programa, evitar resultados erróneos y controlar de forma más clara las condiciones de finalización mediante break.

También se decidió trabajar con un diccionario de preguntas y respuestas, ya que esta estructura facilitaba asociar cada pregunta con su única respuesta correcta. Posteriormente, ese diccionario se transformó en una lista para poder mezclar las preguntas de forma aleatoria antes de empezar la partida.

Por otro lado, se incorporó una limpieza básica de textos en las respuestas del usuario, utilizando métodos como ```strip()``` y ```lower()```, con el objetivo de hacer la comparación más flexible y evitar errores por mayúsculas o espacios innecesarios.

Además, se exploró la posibilidad de diseñar una interfaz muy sencilla en Jupyter Notebook para hacer el juego más visual e intuitivo. Aunque la lógica principal del proyecto está desarrollada en Python, esta idea surge como una línea de mejora para acercar el juego a una experiencia más amigable para la persona usuaria.

Finalmente, se decidió mantener una mecánica simple: una única oportunidad por pregunta y un sistema global de victoria o derrota, en el que el juego termina al alcanzar 5 aciertos o 3 fallos. 

### Retos afrontados

- La indentación:
En algunos momentos, el código no funcionaba bien debido a errores en la estructura de bloques (```ìf```, ```for```, etc.), lo que afectaba al flujo del programa.
- Uso inicial del bucle ```while```:
En un primer planteamiento, se introdujo el bucle ```while```para controlar el flujo del juego, pero estaba dando resultados érroneos. Finalmente, se optó por usar solo el bucle ```for```, que resultó adecuado para iterar sobre la lista de preguntas y controlar el final del juego mediante condiciones y ```break```.


# Historias de usuario
## Historia de usuario 1: jugar al trivial de geografía

**Objetivo**:
Como usuario, quiero responder preguntas de geografía para poner a prueba mis conocimientos y divertirme.

**Descripción**:
En el proyecto, se nos pide la tarea de crear un juego de preguntas y respuestas de geografía usando Python. Teresa y Beatriz deben desarrollar el código fuente del juego, que incluye su lógica y una sencilla interfaz. Este consiste en que el usuario interactúa con el juego respondiendo a preguntas que aparecen por pantalla. El sistema recoge sus respuestas y le indica si son correctas o incorrectas, llevando la cuenta de sus aciertos y fallos.

**Criterios de aceptación**:

- El juego debe mostrar preguntas de forma clara
- El usuario debe poder introducir una respuesta por teclado
- El sistema debe indicar si la respuesta es correcta o incorrecta
- El sistema debe tener un contador de aciertos y errores
- El usuario debe ver el resultado al finalizar el juego


## Historia de usuario 2: jugar al ahorcado

**Objetivo**:

**Descripción**:


**Criterios de aceptación**:

## Historia de usuario 2: jugar a piedra, papel, tijera

**Objetivo**:

**Descripción**:


**Criterios de aceptación**:
