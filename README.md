# Reglas de Autómatas Celulares - Regla 90 y 184

Simulación visual de los autómatas celulares **Regla 90** y **Regla 184** en Java utilizando `Swing`. Se representa una cuadrícula de botones donde se observa la evolución de los patrones al seleccionar la configuración inicial.

## Cómo usar

1. Ejecuta el programa.
2. Selecciona la regla a aplicar desde el `ComboBox`.
3. Activa o desactiva manualmente las celdas de la **primera fila**.
4. El patrón se genera automáticamente.
5. Observa cómo evoluciona el autómata en la cuadrícula.

## Características

- Interfaz visual mediante `Swing` con cuadrícula de 15x15 botones.
- Permite seleccionar manualmente la primera fila como configuración inicial.
- Reglas seleccionables mediante `ComboBox`:
  - Rule 90 (fractales)
  - Rule 184 (movimiento / desplazamiento)
- Actualización automática tras cada clic.
- Visualización intuitiva del comportamiento evolutivo.

---

## ¿Qué son las Reglas 90 y 184?

### Rule 90

La **Regla 90** es un autómata celular unidimensional elemental propuesto por Stephen Wolfram.
Funciona mediante una regla binaria muy simple:
Una celda en la siguiente generación estará activa (`1`) **si y solo si sus vecinos izquierdo y derecho son distintos**.
Si son iguales, la celda estará inactiva (`0`).

Esta regla genera patrones que parecen triángulos fractales, relacionados con el **triángulo de Sierpinski**.
El comportamiento es puramente determinista, por lo que pequeñas variaciones en la primera fila pueden cambiar totalmente el resultado final.

| Vecino izquierdo | Celda actual | Vecino derecho | Siguiente estado |
| ---------------- | ------------ | -------------- | ---------------- |
| 1                | x            | 0              | 1                |
| 0                | x            | 1              | 1                |
| 0                | x            | 0              | 0                |
| 1                | x            | 1              | 0                |

(Sólo importa izquierda y derecha, no la celda actual)

Visualmente, produce patrones con apariencia de zig-zag y simetría.

### Rule 184

La **Regla 184** es también un autómata celular elemental, pero su comportamiento es distinto al de la Regla 90.
Está asociada frecuentemente con **modelos de tráfico** porque simula desplazamientos de partículas a la derecha.

* Una celda encendida (`1`) representa un coche (o partícula).
* Una celda apagada (`0`) representa un espacio vacío.
* Si un coche puede avanzar (la celda a su derecha está vacía), lo hace en la siguiente generación.
* Si no puede avanzar (otro coche bloquea el paso), se mantiene en su posición.
* Los huecos se "llenan" desde la izquierda si había un coche detrás.

Esto permite observar cómo grupos de elementos se desplazan, se acumulan o se liberan.

| Izquierda | Centro | Derecha | Siguiente estado |
| --------- | ------ | ------- | ---------------- |
| 1         | 0      | 0       | 1                |
| 0         | 1      | 0       | 0                |
| 1         | 1      | 0       | 0                |
| 1         | 1      | 1       | 1                |
| 0         | 0      | 1       | 0                |
| 0         | 0      | 0       | 0                |
