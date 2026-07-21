# Piano Phase — Visualizador de Phasing

Una visualización interactiva en el navegador (HTML + Canvas + Web Audio, sin dependencias externas) inspirada en *Piano Phase* (1967), de Steve Reich.

🔗 **[Ver el proyecto en vivo](https://tu-usuario.github.io/tu-repo/)**


## Qué es esto

En 1967, Steve Reich escribió *Piano Phase* para dos pianistas tocando la misma célula de doce notas. La idea nació de un accidente: en sus primeras piezas con cinta, dos grabadoras idénticas se desincronizaban solas, por las pequeñas diferencias mecánicas entre una y otra. Reich se preguntó qué pasaría si llevaba ese accidente a un escenario, con dos personas en vez de dos máquinas. La partitura no da ningún número: solo le pide a uno de los dos pianistas que acelere gradualmente, de oído, hasta encontrar de nuevo al otro, un pulso más adelante.

Este proyecto es un experimento personal: toma esa misma idea y le pone un número fijo (un desfase de velocidad del 2%) para ver qué forma toma cuando se convierte en espiral.

## Qué incluye

- **Espiral de phasing**: dos trazados de la misma célula de 12 notas, uno de referencia y otro desfasándose gradualmente, con color propio para cada nota. Se realinean por completo cada ~2 minutos y 13 segundos.
- **Dos teclados espejados**: un piano (rango Do4–Re5) por cada voz, uno normal y otro invertido verticalmente, encendiendo la tecla real que suena en cada momento.
- **Sonido generado en tiempo real** con la Web Audio API (síntesis aditiva, sin samples ni librerías externas) — nada de audio pregrabado.
- **Metrónomo visual y compás de alzar** (LED, sin clic audible) para ayudar a sincronizar con otras herramientas si lo necesitas.
- Controles de **inicio/reinicio**, **silenciar** y **volumen**.

## Cómo usarlo

Es un único archivo HTML autocontenido. Solo necesitas abrirlo en un navegador moderno (Chrome, Edge, Firefox):

```bash
# opción simple
abre el archivo .html haciendo doble clic

# o, si prefieres servirlo localmente
python3 -m http.server 8000
# luego visita http://localhost:8000/nombre-del-archivo.html
```

No requiere build, no requiere `npm install`, no depende de ningún CDN.

## Stack técnico

- HTML5 Canvas para todo el dibujo (espiral, teclados, fondo con textura de grano)
- Web Audio API para la síntesis de sonido (osciladores + filtros, sin muestras de audio)
- Vanilla JavaScript, sin frameworks ni librerías

## Créditos

- **Composición e idea original**: Steve Reich, *Piano Phase* (1967)
- **Programación musical / prototipado del concepto sonoro**: [Strudel](https://strudel.cc)
- **Visualización e implementación de este proyecto**: hecho con ayuda de [Claude](https://claude.ai) (Anthropic)

Este es un proyecto de exploración personal, no una versión oficial ni autorizada de la obra de Steve Reich.

## Licencia

<!-- elige la que prefieras, por ejemplo: -->
MIT — el código es libre de usar, modificar y compartir. La obra musical original (*Piano Phase*) sigue protegida por los derechos de su compositor.