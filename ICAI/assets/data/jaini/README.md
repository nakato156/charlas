# Jaini, Clark y Geirhos (2024), Fig. 6

Fuente: https://proceedings.iclr.cc/paper_files/paper/2024/file/3ba4d47a83e498c2b1a0868cba20f6de-Paper-Conference.pdf,
página 7. `figure6-original.png` es el raster original extraído del objeto PDF
19 (2032 × 1368), no una ampliación de los PNG anteriores sin etiquetas.

`scripts/prepare_matrix.py` recorta la matriz completa con su marco de orientación
y el bloque inferior derecho (18 × 18). Conserva los píxeles originales, orden,
colores y celdas. Reconstruye etiquetas completas en las filas y usa números en
columnas, referidos explícitamente a los mismos evaluadores en el mismo orden.
El bloque contiene CLIP, Parti, Noisy Student, ViT-22B, Imagen, Stable Diffusion
y diez observadores humanos. No todos sus modelos son generativos.
Los nombres de sujetos se adaptan a «Observador NN», manteniendo su orden original.
