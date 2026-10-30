# Combates espaciales

Juego de estrategia y puntería por turnos en el que te enfrentas a una nave controlada por el ordenador. Ajusta el ángulo y la potencia de tus misiles para destruir al enemigo mientras los campos gravitatorios de los objetos cósmicos alteran sus trayectorias.

## Características

- **Jugador contra ordenador:** cada nave dispara por turnos.
- **Disparos configurables:** selecciona el ángulo y la potencia antes de lanzar cada misil.
- **Gravedad:** estrellas, planetas, agujeros negros, enanas blancas y nebulosas atraen los proyectiles.
- **Escenarios aleatorios:** los objetos cósmicos y la posición vertical de las naves cambian en cada partida.
- **Trayectorias visibles:** sigue la estela del misil para ajustar tu siguiente disparo.
- **IA progresiva:** el ordenador simula combinaciones de ángulo y potencia, refina sus mejores intentos y reduce su imprecisión a medida que avanzan los turnos.
- **Efectos visuales:** fondo estrellado animado, resplandores, partículas y explosiones.

## Requisitos

- Un navegador moderno con JavaScript habilitado y soporte para Canvas 2D.
- Ratón o panel táctil para manejar los controles.
- Se recomienda una pantalla con espacio suficiente para el área de juego de **1200 × 700 píxeles**, más sus bordes.

No es necesario instalar dependencias, compilar el proyecto ni disponer de conexión a Internet para jugar con los archivos locales.

## Cómo ejecutar el juego

1. Descarga o copia los archivos del proyecto en tu equipo.
2. Abre [`index.html`](index.html) en el navegador, por ejemplo, haciendo doble clic sobre el archivo.
3. Pulsa **Jugar** para comenzar la partida.

## Cómo jugar

Tu nave es la **azul**, situada a la izquierda. La nave del ordenador es la **roja**, situada a la derecha. El jugador realiza el primer disparo.

1. Observa la posición del enemigo y los objetos cósmicos que hay entre las dos naves.
2. Ajusta el **ángulo** y la **potencia** con los controles deslizantes. La flecha junto a tu nave indica la dirección inicial del disparo.
3. Pulsa **Disparar** y observa la trayectoria del misil.
4. Si el disparo no destruye ninguna nave y termina al chocar con un objeto cósmico o salir de los límites del escenario, el turno pasa al rival.
5. Utiliza lo aprendido de cada trayectoria para corregir el siguiente lanzamiento.
6. Al terminar la partida, pulsa **Nueva Partida** para generar otro escenario y volver a jugar.

### Controles

| Control | Función |
| --- | --- |
| **Ángulo** | Establece la dirección inicial del misil, de 0° a 360°. |
| **Potencia** | Establece la velocidad inicial del misil, con valores de 50 a 500. |
| **Disparar** | Lanza un misil durante tu turno. |
| **Jugar** | Inicia la partida desde la pantalla de bienvenida. |
| **Nueva Partida** | Inicia otra partida después de una victoria o derrota. |

Los ángulos se interpretan así: **0° y 360° hacia la derecha**, **90° hacia arriba**, **180° hacia la izquierda** y **270° hacia abajo**.

### Reglas de victoria y derrota

- Un único impacto destruye una nave. Gana quien conserve su nave intacta.
- Los campos gravitatorios modifican la dirección y la velocidad de los misiles durante el vuelo.
- Si un misil golpea un objeto cósmico, desaparece y el turno pasa al rival.
- Si un misil sale de los límites del escenario, el turno también pasa al rival.
- **Existe fuego propio:** si tu misil regresa e impacta contra tu nave, gana el ordenador. El ordenador también puede destruirse con su propio disparo.

### Consejos

- Apuntar directamente al enemigo no siempre funciona: ten en cuenta la atracción de los objetos cercanos a la trayectoria.
- Prueba pequeños cambios de ángulo y potencia entre disparos para entender el efecto de la gravedad.
- La flecha de apuntado muestra la dirección inicial, no la trayectoria completa que seguirá el misil.
- Vigila los disparos que se curvan hacia tu propia nave.

## Tecnologías

- **HTML5 y Canvas 2D:** estructura de la interfaz y dibujo del escenario.
- **CSS3:** estilos, controles y efectos de la interfaz.
- **JavaScript:** física gravitatoria, colisiones, inteligencia artificial y animación mediante `requestAnimationFrame`.

El juego está implementado en un único archivo `index.html`, con los estilos y el código JavaScript integrados, sin bibliotecas externas.

## Archivos principales

| Archivo | Descripción |
| --- | --- |
| [`index.html`](index.html) | Juego completo: interfaz, renderizado, lógica y comportamiento del ordenador. |
| [`Requisitos.md`](Requisitos.md) | Requisitos originales de diseño del juego. |
| [`README.md`](README.md) | Descripción del proyecto e instrucciones para jugar. |
