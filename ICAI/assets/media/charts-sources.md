# Gráficos compartidos de la migración Quarto

Los cuatro gráficos PNG redibujan las barras de `p2` conservando cifras y
etiquetas. Son figuras científicas compartidas por Reveal.js y PowerPoint.
Las etiquetas y cifras también constan como `fig-alt` en `presentacion.qmd`.

- `forma.png`: Jaini, Clark y Geirhos (2024), Fig. 1 y Tabla 1. ResNet-50 21%,
  CLIP (80 prompts) 57%, Stable Diffusion 93%, humanos 96%, Imagen 99%.
- `errores.png`: mismo trabajo, Tabla 1. κ de coincidencia de acierto/error:
  ResNet-50 0,21, ViT-22B-384 0,26, CLIP (80 prompts) 0,28, Imagen 0,31.
- `alcance.png`: Kamath et al. (2024), Tabla 3, experimento 1A. Coincidencia
  con la lectura mayoritaria: humanos 90%, Llama 2 70B 88%, GPT-3.5 td003 91%,
  GPT-4 98%. No son resultados sobre la adaptación española.
- `cobertura.png`: Srikanth et al. (2025), §6. Cobertura media por respuesta:
  humanos 44%, modelos 77%. No es una medida de precisión.

Las referencias completas y los enlaces originales se conservan en el `.qmd`.
Los paneles originales de Hu et al. conservan su procedencia en
`language-sources.md`. Las restantes figuras reutilizan los recursos de `p2`.

## Revisión focalizada de octubre de 2026

`hu-irony.png`: calculado desde los datos de Hu et al. (2023). Dos categorías,
dos series, medias originales e IC 95%, sin renormalizar distractores omitidos.
Procedimiento y cifras: `../data/hu/README.md`. El PPTX usa un gráfico nativo
equivalente con libro incrustado, desde el mismo `summary.json`.

`jaini-matrix-full.png` y `jaini-matrix-zoom.png`: Fig. 6 recuperada del PDF
original. Celdas, orden y colores conservados. Etiquetas completas reconstruidas,
columnas numeradas con correspondencia a filas. Procedencia: `../data/jaini/README.md`.
Los paneles antiguos se conservan como recursos históricos y ya no se muestran.

## s20: sustitución por figura publicada

`hu-2023-figure1.png` sustituye el gráfico calculado de ironía en la presentación vigente. Es un recorte directo de la figura 1 de Hu et al. (ACL 2023), p. 4199, sin redibujar barras ni recalcular cifras o intervalos. La medida es proporción de respuestas correctas. Procedencia: `assets/data/hu/figure1-source.json`. `hu-irony.png` y su gráfico nativo quedan como históricos.
