# Gestión del agua en un tanque comunitario

**Estudiante:** Carlos Alejandro Salgado Llusco · **Asignatura:** INF-373 Métodos Numéricos I · **Desafío individual:** modelar un problema real con EDO de primer orden

Aplicación web que simula el volumen de agua de un tanque comunitario y compara la solución analítica con los métodos de Heun (RK2) y Runge-Kutta de 4.º orden (RK4).

## Descripción del modelo
- Variable independiente: `t`, tiempo (h). Variable dependiente: `V(t)`, volumen almacenado (L).
- EDO: `dV/dt = Qe − Qc − k·V`, con condición inicial `V(0) = V₀`.
- Solución analítica: `V(t) = a/k + (V₀ − a/k)·e^(−kt)`, con `a = Qe − Qc`.
- Parámetros hipotéticos por defecto: V₀ = 2000 L, Qe = 400 L/h, Qc = 250 L/h, k = 0,03 1/h, capacidad = 6000 L, T = 24 h, h = 2 h. Con ellos: `dV/dt = 150 − 0,03·V` y `V(t) = 5000 − 3000·e^(−0,03t)`.
- Supuestos: caudales constantes, pérdida proporcional al volumen, sin desborde. Es una simulación, no una predicción con datos reales.

## Funciones
Ajuste de parámetros con validación y unidades; Heun y RK4 con el mismo h; tanque animado; gráfica comparativa; tabla por pasos con error absoluto y relativo (%); resultados e interpretación automática.

## Cómo ejecutarla
No requiere instalación: abrir `index.html` en un navegador, o usar la versión publicada con GitHub Pages (Settings → Pages → rama principal).

## Archivos
- `index.html`: aplicación completa (HTML, CSS y JavaScript, sin dependencias externas).
- `README.md`: esta descripción.
