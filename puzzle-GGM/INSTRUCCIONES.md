# 🧩 Instrucciones del Rompecabezas de Imagen

Bienvenido al juego de rompecabezas web. El objetivo principal es rearmar una imagen subida por ti, intercambiando las posiciones de las piezas que la componen.

---

## 🎯 Objetivo del Juego
Reordenar todas las piezas del tablero hasta que la imagen original se muestre correctamente.

---

## 1. Flujo de Configuración

Antes de empezar, debes configurar el rompecabezas en el formulario inicial:

### 1.1. Subir Imagen
Utiliza el campo **"1. Selecciona la Imagen (*)"** para subir cualquier archivo de imagen (JPG, PNG, etc.) desde tu dispositivo.

### 1.2. Tamaño del Rompecabezas
Define la complejidad seleccionando el número de **Filas** y **Columnas**.

- **Mínimo:** 2x2  
- **Máximo:** 20x20  
- **Sugerencia:** 4x4 es un buen punto de partida.

### 1.3. Límite de Tiempo (Opcional)
Puedes introducir un valor en **Minutos** para establecer un cronómetro de cuenta regresiva.

- Si el tiempo llega a cero antes de completar el puzzle, **perderás la partida**.
- Si se deja vacío, el juego tendrá **tiempo ilimitado** (solo se contará el tiempo transcurrido).

Una vez configurado, presiona **"Iniciar Rompecabezas"**. El sistema cortará y mezclará las piezas automáticamente.

---

## 2. Mecánica del Juego

### 2.1. El Tablero
La imagen mezclada se mostrará en el **Tablero de Juego** (el Canvas principal).  
La imagen se escalará para que el tablero sea cuadrado, manteniendo la proporción original de las piezas.

### 2.2. Vista Previa
En el panel de información lateral verás la **Vista Previa Original**.  
Úsala como referencia visual para saber cómo debe lucir el puzzle terminado.

### 2.3. Movimiento de Piezas (Drag & Drop)

- **Arrastrar (Drag):** Haz clic o toca una pieza y arrástrala. Verás un efecto de sombra en la pieza que estás moviendo.  
- **Intercambiar (Drop):** Suelta la pieza que estás arrastrando sobre la pieza con la que deseas intercambiar la posición.  
- Un **indicador amarillo** te mostrará dónde se soltará la pieza.  
- Después de cada intercambio exitoso, el contador de **Movimientos** aumentará en 1.

### 2.4. Estadísticas
El juego rastrea dos métricas clave:

- **Tiempo Transcurrido:** Muestra cuánto tiempo llevas jugando.
- **Cronómetro (TimerDisplay):**
  - Si definiste un límite, muestra el tiempo restante (cuenta regresiva).
  - Si no definiste un límite, muestra el tiempo transcurrido.

---

## 3. Finalización del Juego

El juego puede terminar de dos maneras:

### 3.1. ¡Ganaste! (Condición de Victoria)
El juego termina cuando la propiedad `currentPos` de cada pieza coincide con su `originalPos`.

### 3.2. Perdiste (Condición de Derrota)
Solo ocurre si configuraste un límite de tiempo y este llega a cero.

### 3.3. Modal de Resultado
Al finalizar, aparecerá un modal mostrando tu rendimiento:

- **Tiempo Total:** El tiempo que tardaste en completarlo o hasta la derrota.
- **Movimientos:** Cantidad de intercambios realizados.

Desde el modal puedes elegir:

- **"Subir Nueva Imagen":** Vuelve a la pantalla de configuración inicial.  
- **"Jugar de Nuevo (Misma Imagen)":** Mezcla nuevamente las piezas con la misma configuración y reinicia el cronómetro sin cambiar la imagen.

---
