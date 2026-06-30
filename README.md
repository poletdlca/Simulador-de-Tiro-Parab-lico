# Simulador de Tiro Parabólico 

## Física implementada

- Tiempo de vuelo: `T = 2·v0·sin(θ)/g`
- Altura máxima: `H = (v0·sin(θ))² / (2g)`
- Alcance máximo: `R = v0²·sin(2θ) / g`
- Posición en el instante *t*:
  - `x(t) = v0·cos(θ)·t`
  - `y(t) = v0·sin(θ)·t − ½·g·t²`

## Búsqueda binaria del ángulo óptimo

`R(θ) = v0²·sin(2θ)/g` es creciente en `[0°, 45°]` y decreciente en
`[45°, 90°]`. Por eso la búsqueda binaria se restringe al tramo `[0°, 45°]`
(donde la función es monótona) para encontrar el ángulo que produce un
alcance lo más cercano posible al alcance objetivo solicitado.

## Uso del menú

1. Simular nuevo lanzamiento (ingresa velocidad, ángulo, gravedad, masa y dt)
2. Mostrar resumen del último lanzamiento (tiempo de vuelo, altura y alcance)
3. Guardar trayectoria en CSV (para graficar después, ej. en Python/Excel)
4. Guardar trayectoria en archivo binario
5. Cargar trayectoria desde archivo binario
6. Verificar si el proyectil impacta en un blanco ubicado en una posición x
7. Buscar el ángulo óptimo para alcanzar una distancia objetivo (búsqueda binaria)
