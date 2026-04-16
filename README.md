# PROMO-67---EQUIPO-1---PROYECTO-MODULO-1

# Proyecto Mini Classic Games

**Mini Classic Games** es una colección de tres juegos clásicos desarrollados en formato **Jupyter Notebook (.ipynb)** por el equipo **STBR Data**. Este proyecto busca ofrecer una experiencia de entretenimiento sencilla, dinámica e interactiva para un público amplio.

## 🚀 Sobre el Proyecto
- **Formato:** Entrega de 3 cuadernos interactivos independientes para facilitar la ejecución y visualización del código.
- **Metodología:** Desarrollo bajo el marco de trabajo **Scrum** por el equipo **STBR Data** (4 desarrolladoras), asegurando un producto funcional, testeado y documentado.
- **Tecnología:** Python 3, optimizado para su ejecución en entornos de desarrollo interactivos como Jupyter Notebook y VS Code.

---

## 🎮 Catálogo de Juegos

## 1. El Juego del Ahorcado

### 1.1. Descripción general
El **Juego del Ahorcado** es un clásico juego de adivinanza de palabras. El jugador debe descubrir la palabra secreta letra por letra antes de quedarse sin intentos.

**Características principales:**
- El juego se desarrolla y juega en Python y en español.
- La base de datos cuenta con **300 palabras** distribuidas en categorías como: ROPA, TECNOLOGÍA, ANIMALES, COMIDA, CIUDADES, DEPORTES, COLEGIO/UNIVERSIDAD, HOGAR, PROFESIONES, VIAJES, NATURALEZA, EMOCIONES, OCIO Y TIEMPO.
- Hay 6 intentos por partida, con representación visual del “ahorcado” en cada error iniciando con la cabeza del personaje.
- Retroalimentación dinámica y mensajes motivadores durante el juego.

### 1.2. Cómo jugar
1. Ejecutar el archivo que contiene el juego.
2. Introducir **una letra** por turno.
3. El juego indicará si la letra es correcta y actualizará la visualización.
4. La partida termina cuando se adivina la palabra (**victoria**) o se acaban los 6 intentos (**derrota**).

**Reglas adicionales:**
- Conversión automática de mayúsculas y tildes para evitar errores de usuario.
- Las letras repetidas se notifican, pero no restan intentos.
- **Nota:** En Jupyter Notebook, si el output se trunca tras varios intentos, ajustar la celda a "scrollable".

### 1.3. Detalles técnicos y funciones principales
- **`juego_ahorcado()`** -> Función principal que controla el flujo, gestiona el bucle de eventos y evalúa las condiciones de victoria o derrota.
- **Variables importantes:**
  - `palabra_secreta` -> Palabra elegida aleatoriamente de la lista de 300 términos.
  - `letras_adivinadas` -> Lista que almacena las letras introducidas por el jugador.
  - `intentos` -> Número de oportunidades restantes (inicialmente 6).
  - `palabra_mostrada` -> Visualización dinámica de la palabra con letras descubiertas y guiones bajos.
- **Funciones internas y lógica:**
  - Comprobación de la letra: Validación de caracteres válidos y control de uso previo.
  - Renderizado: Gestión de los intentos y dibujo progresivo del ahorcado en ASCII.

### 1.4. Posibles mejoras futuras
- Implementar interfaz gráfica y añadir emoticonos para mayor atractivo visual.
  
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
También hemos solucionado que se escriba la palabra sin tilde, mediante una función def.

### Decisiones de diseño
Durante el desarrollo del proyecto se tomaron varias decisiones para simplificar la lógica del juego y hacerlo más funcional.

En primer lugar, aunque inicialmente se intentó controlar el flujo del juego mediante un bucle ```while```, finalmente se optó por utilizar un bucle ```for``` para recorrer las preguntas. Esta decisión permitió organizar mejor la lógica del programa, evitar resultados erróneos y controlar de forma más clara las condiciones de finalización mediante break.

También se decidió trabajar con un diccionario de preguntas y respuestas, ya que esta estructura facilitaba asociar cada pregunta con su única respuesta correcta. Posteriormente, ese diccionario se transformó en una lista para poder mezclar las preguntas de forma aleatoria antes de empezar la partida.

Por otro lado, se incorporó una limpieza básica de textos en las respuestas del usuario, utilizando métodos como ```strip()``` y ```lower()``` y una función def, con el objetivo de hacer la comparación más flexible y evitar errores por mayúsculas, espacios innecesarios y tildes.

Además, se exploró la posibilidad de diseñar una interfaz muy sencilla en Jupyter Notebook para hacer el juego más visual e intuitivo. Aunque la lógica principal del proyecto está desarrollada en Python, esta idea surge como una línea de mejora para acercar el juego a una experiencia más amigable para la persona usuaria.

Finalmente, se decidió mantener una mecánica simple: una única oportunidad por pregunta y un sistema global de victoria o derrota, en el que el juego termina al alcanzar 5 aciertos o 3 fallos. 

### Retos afrontados

- La indentación:
En algunos momentos, el código no funcionaba bien debido a errores en la estructura de bloques (```ìf```, ```for```, etc.), lo que afectaba al flujo del programa.
- Uso inicial del bucle ```while```:
En un primer planteamiento, se introdujo el bucle ```while```para controlar el flujo del juego, pero estaba dando resultados érroneos. Finalmente, se optó por usar solo el bucle ```for```, que resultó adecuado para iterar sobre la lista de preguntas y controlar el final del juego mediante condiciones y ```break```.


