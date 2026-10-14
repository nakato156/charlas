# Hu et al. (2023), Fig. 3: ironía

Datos originales de https://github.com/jennhu/lm-pragmatics:
`human_data/fj/Human_Irony.csv`, `fj_raw_data/IronyKeyComplex.txt` y los cinco
`model_data/Irony_text-davinci-002_seed{0..4}_examples0.csv` principales.
No se usan los archivos `no-story`.

Procedimiento: https://github.com/jennhu/lm-pragmatics/blob/master/analysis/main.ipynb,
funciones `update_complex_labels` y `get_answer_distributions`, y el barplot de
`answer_dists.pdf` (Fig. 3). `compute_hu.py` usa la clave compleja actualizada y
el orden aleatorio de opciones. Frecuencias humanas por estímulo, media de 25
estímulos. Probabilidades del modelo por estímulo y permutación, media de 125
filas: equivale a promediar cinco permutaciones de cada uno de 25 estímulos.
El gráfico muestra dos categorías y omite distractores sin renormalizar.

Bootstrap percentil del 95%, 1000 remuestreos de filas con reemplazo, media como
estimador: procedimiento predeterminado del `seaborn.barplot` usado en el
notebook, sin variable `units`. Para reproducibilidad se fija semilla 20261008
con NumPy `default_rng`; se usa la misma semilla para cada barra. El notebook
no fija una semilla, por lo que sus extremos de IC pueden variar ligeramente.
Este procedimiento NO agrupa las cinco permutaciones por estímulo para el IC
ni remuestrea participantes humanos. No debe interpretarse como tal.

La clave original contiene una etiqueta distractora duplicada en un estímulo.
Se conserva tal cual, como el notebook. No afecta a las dos categorías mostradas.
El notebook usa la primera posición para un distractor duplicado; no se usa
esa distribución incompleta para renormalizar las categorías seleccionadas.

`summary.json` registra medias con toda su precisión, IC y SHA256 de los siete
archivos. `scripts/compute_hu.py` regenera el resumen y `hu-irony.png`.
`scripts/native_hu_chart.py` crea el gráfico horizontal editable y un libro XLSX
incrustado, con medias, extremos y diferencias para sus barras de error.

| Serie | Pragmática correcta (IC 95%) | Literal (IC 95%) |
|---|---|---|
| Humanos, frecuencia | 0,919465 (0,888981–0,945136) | 0,056578 (0,036465–0,080757) |
| text-davinci-002, probabilidad | 0,582010 (0,499722–0,659077) | 0,398578 (0,321487–0,477399) |

## s20 vigente: figura 1 original

Desde la revisión del 9 de octubre de 2026, s20 muestra `assets/media/hu-2023-figure1.png`, un recorte directo de la figura 1 del PDF original (p. 4199), conservado en `2023.acl-long.230.pdf`. `figure1-source.json` registra coordenadas y hash. No hay medias ni intervalos calculados para esta figura. Los archivos y resultados de la figura 3 descritos arriba se conservan como históricos y ya no aparecen en la presentación.

La medida visible es proporción de respuestas correctas para ambos grupos; en modelos, el criterio publicado es asignar la mayor probabilidad al token de la opción correcta (§4.1). La revisión de fuentes posteriores está en `docs/research/2026-10-09-ironia-comparacion-actualizada.md`.
