# Regla 90 - Autómata Celular

Simulación visual del autómata celular **Regla 90** utilizando Java y `Swing`. El programa muestra una cuadrícula de botones, donde el usuario puede establecer la primera fila y observar cómo evoluciona el patrón de acuerdo con la regla.

## ¿Qué es la Regla 90?

La Regla 90 es un autómata celular unidimensional definido por Stephen Wolfram. Genera patrones fractales a partir de reglas simples aplicadas a celdas binarias (encendido/apagado). El estado de una celda en la siguiente fila depende exclusivamente de las celdas vecinas izquierda y derecha de la fila anterior.

## Características

- Interfaz gráfica hecha con `Swing`.
- Botones representan celdas: blancas (apagadas) o negras (encendidas).
- El usuario selecciona la configuración inicial en la primera fila.
- La evolución del autómata se genera automáticamente al hacer clic.
- Visualización clara de cómo la regla 90 transforma los patrones.

## Cómo usar

1. Ejecuta el programa.
2. Haz clic en los botones de la **primera fila** para activar (negro) o desactivar (blanco) las celdas iniciales.
3. El patrón se genera automáticamente después de cada clic.
4. Observa cómo se dibuja el patrón a lo largo de las filas.