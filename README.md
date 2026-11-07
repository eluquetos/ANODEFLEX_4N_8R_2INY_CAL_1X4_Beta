# ANODEFLEX_4N_8R_2INY_CAL_1X4_v1.0.1

Aplicación para calcular las resistencias de ocho ramas a partir de dos mediciones de campo independientes y regularlas con una sola inyección.

## Mediciones de campo

- Lado A: VA → Rc1 → nodo 1 → Rc2 → nodo 2; ramas 11, 12, 21 y 22.
- Lado B: VB → Rc3 → nodo 3 → Rc4 → nodo 4; ramas 31, 32, 41 y 42.

La calibración conserva el cálculo de ANODEFLEX_4N_8R_2INY_CAL_2X2N_v1.0.1. Las dos mediciones se realizan con los reóstatos en 0 Ω.

## Regulación

Una fuente independiente alimenta desde el nodo 1 los cuatro tramos Rc1 a Rc4 en secuencia. El voltaje de regulación es una entrada propia: no es la suma de VA y VB. La aplicación calcula el voltaje mínimo y los reóstatos para las ocho corrientes objetivo, o permite ajustar el voltaje y los reóstatos manualmente. Un ajuste que supera el máximo configurado se declara inviable.

Los casos se pueden exportar e importar como archivos JSON. GitHub Pages sirve la carpeta `docs`.

## Comprobación

Ejecute `node tests/model.test.js` y `node tests/static.test.js`.
