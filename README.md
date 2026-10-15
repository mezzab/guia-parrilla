# Guía del tiraje — Parrilla argentina

Guía interactiva para dimensionar la trampa de humo (pulmón, garganta, cámara, campana y caño) de una parrilla de obra argentina de boca grande, pensada para un quincho cerrado sin extractor.

- **Proyecto:** Parrilla argentina · **Lámina:** Guía del tiraje · **Autor:** Marcos Mezzabotta
- **Guía en línea:** <https://mezzab.github.io/guia-parrilla/> (GitHub Pages, se actualiza con cada push a `main`).
- **Sin conexión:** descargar `index.html` y abrirlo en cualquier navegador; es un único archivo sin dependencias (la tipografía Barlow, familia DIN, va embebida).

## Qué hay adentro

1. **Diseñá la tuya** — arriba de todo: tablero con sliders (boca, losa y techo, hogar, dintel, pulmón, campana y caño con el diámetro también en pulgadas), corte y frente a escala, veredicto contra todas las reglas con lo recomendado al lado, y tabla de medidas para el albañil.
2. **¿Querés entender más?** — entrada a la guía detallada:
   - **Partes** — corte con cada elemento numerado.
   - **Física** — por qué tira: efecto chimenea, penacho y arrastre de aire, garganta laminar (Rumford).
   - **Boca · Pulmón · Garganta · Cámara · Campana · Caño · Aire** — cada sección explica la regla, la física detrás y muestra un par *bien / mal* dibujado a escala.
   - **Lo que aprendimos** — conclusiones al reconciliar fuentes que miden desde puntos distintos.

Valores fijos (no son controles): hondura de la copa 15 cm, alto del dintel 26 cm, caño de 4 m, gases a 200 °C.

## Reglas resumidas (todo referido a la boca)

| Elemento | Regla |
|---|---|
| Boca | alto ≤ 70 cm |
| Caño | ≥ 10 % del área de la boca si es redondo, ≥ 15 % si es cuadrado; 12–13 % recomendado |
| Garganta | 10–15 cm de ancho (ref. 12); área ≥ área del caño |
| Pulmón | arranca a ≥ 50 % del alto de la boca, nunca por encima; 30–35° con la vertical (hasta 45°) |
| Copa | media caña de 15–25 cm de hondo sobre el pulmón; ahí gira el aire que baja por el fondo |
| Altura de la garganta | 20–40 cm sobre la boca y por encima del fin del pecho |
| Pecho | radio 15–20 cm en la esquina interior del dintel |
| Pared recta | 15–20 cm por encima de la garganta antes de que cierre la campana |
| Campana | tres caras inclinadas, laterales ≤ 45° con la vertical, fondo vertical, caño pegado atrás y recto |
| Remate | ≥ 1 m sobre la cumbrera |

Las fuentes (KATZ, Asando, ParriSur, TEORICA10, Buckley Rumford, BIA, NFPA 211, Morton–Taylor–Turner 1956, Solid Fuel UK) están enlazadas al pie de la guía.

## Desarrollo

Todo vive en `index.html`: CSS con tokens claro/oscuro, SVG generado por JavaScript a partir de las medidas (`EX` son los valores por defecto, `derive()` calcula el plano, `corte()`/`frente()` dibujan). El estado del tablero se guarda en `localStorage`.
