Utilice la tecnica de meta prompt para llegar al resultado del primer prompt:

IA: Gemini
LLM: Flash 2.5



0.- 

Ayudame a hacer un prompt para darselo a gemini - flash 2.5 y me ayude a construir un juego con Canvas, este es el prompt que tengo: Eres un experto en HTML + CSS + Tailwind Te solicitaron un videojuego en el cual seguira la siguiente dinamica: El juego trata de un rompecabezas (cuadros), el cual se forma de una imagen que el usuario suba, asi mismo, puede colocar un tiempo, y si no acaba en este tiempo, el usuario pierde (esta funcionalidad es opcional), asi mismo el usuario puede decidir en cuantos cuadros puede partir la imagen (ej: 4x4, 2x2, 18x18, 4x7, etc). El juego termina cuando el usuario logra armar la imagen original de manera correcta. Asi mismo, debe de tener una visualización de la imagen original, para que no se pierda. ¿Como arma el usuario el rompecabezas? R: El usuario va a arrastrar un cuadro a otro y el cuadro al que arrastre, va a tomar el lugar del otro, es decir, se va a intercambiar. 1.- El usuario tendra un formulario al inicio en el cual tendra que colocar la siguiente información: - Subir una imagen - Colocar minutos para cronometro (opcional) 2.- Procede a armar el rompecabezas 3.- Cuando termina ya sea gane o pierda saldra un modal el cual indique el resultado. Cuida mucho la UI/UX y hazme preguntas si tienes dudas.

Justificacion:
Este prompt me sirvio para hacer el seguindo, en este mismo esta difuso actualmente, no mencino tantas cosas como deberia.

1.- 
    Eres un experto en HTML + CSS + Tailwind + JavaScript y en el uso del elemento <canvas> para desarrollar videojuegos web.



    Quiero que me ayudes a construir un videojuego tipo rompecabezas con la siguiente dinámica:



    --------------------------------------

    🎯 Objetivo del juego

    --------------------------------------

    El juego será un rompecabezas generado a partir de una imagen que suba el usuario. El flujo debe ser:



    1. El usuario llena un formulario inicial.

    2. Se genera el rompecabezas según la configuración.

    3. El usuario arma el rompecabezas arrastrando piezas que se intercambian entre sí.

    4. El juego termina cuando:

    - El usuario arma correctamente la imagen (gana), o

    - Se acaba el tiempo del cronómetro si se activó (pierde).



    Debe existir una vista previa de la imagen original como referencia.



    --------------------------------------

    🧩 Mecánica del rompecabezas

    --------------------------------------

    - Usar Canvas para:

    - Dividir la imagen en una cuadrícula configurable (2x2, 4x4, 4x7, 18x18, etc.).

    - Mezclar las piezas.

    - Permitir que el usuario arrastre una pieza y la suelte sobre otra para intercambiar posiciones.



    - Después de cada intercambio, verificar si el rompecabezas está completo.



    - La imagen puede ser de cualquier proporción; debe escalarse sin perder calidad ni distorsionarse.



    --------------------------------------

    🕹️ Flujo completo del juego

    --------------------------------------



    1. Formulario inicial

    Debe incluir:

    - Subir imagen

    - Seleccionar tamaño del rompecabezas (filas x columnas)

    - Minutos opcionales para cronómetro

    Validar datos antes de iniciar.



    2. Juego

    - Renderizar el rompecabezas dentro de un <canvas>

    - Mostrar cronómetro si se activó

    - Mostrar panel con:

        - Número de movimientos

        - Tiempo transcurrido

        - Vista previa de la imagen original



    3. Finalización

    Mostrar un modal:

    - “¡Ganaste!” si completó la imagen

    - “Perdiste” si se acabó el tiempo

    Debe incluir:

    - Tiempo total

    - Movimientos realizados

    Botones:

    - “Jugar de nuevo”

    - “Subir nueva imagen”



    --------------------------------------

    🎨 Requisitos de UI/UX

    --------------------------------------

    - Diseño moderno, claro y responsivo

    - Todo con TailwindCSS

    - Animaciones suaves al mover piezas

    - Estados visuales claros (hover, active, focus)

    - Código limpio, modular y comentado



    --------------------------------------

    🧱 Requisitos técnicos

    --------------------------------------

    - Usar HTML + Tailwind + JavaScript vanilla

    - Organizar el código en:

    - Un archivo HTML principal

    - Un archivo JS externo con funciones para:

        - Cargar imagen

        - Cortarla en piezas

        - Renderizar en canvas

        - Drag & drop

        - Intercambiar piezas

        - Verificar victoria

        - Cronómetro

        - Modal de fin



    --------------------------------------

    📝 Lo que necesito de ti

    --------------------------------------

    1. Propón primero la arquitectura del proyecto.

    2. Luego genera el código completo (HTML + Tailwind + JS).

    3. Si algo no está claro, hazme preguntas antes de asumir.



    Cuida muchísimo la UI/UX y la claridad del código.

    Puedes hacer las preguntas que consideres necesarias para la retroalimentación del juego.


Justificación:
En este prompt se tocaron temas bastante especificos para que el LLM accionara de manera correcta, agrego validaciones, un flujo estandar del usuariom arquitectura.

2.- Fix de 2 errores encontrados:

Al arrastrar me esta saliendo un cuadro de color amarillo (supongo que lo colocaste para saber donde voy a colocar el cuadro, pero actualmente no esta cuadrando bien en el permietro del cuadro. Asi mismo, el tiempo cada que hago un movimiento se resetea a 0 y vuelve a poner el tiempo correcto, puedes hacer que siga contando aun asi este tiempo y que no salga ese 0?

Justificación:
La mayoria de los errores fueron de código en general y los arreglo la IA por si misma, no tuve que involucrarme en general ya que la herramienta me ayuda con el auto repair.