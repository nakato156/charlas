# Amouyal, Meltzer-Asscher y Berant · ACL 2025

Fuente única del nuevo bloque: [artículo original](https://aclanthology.org/2025.acl-long.403/).
El PDF publicado se conserva como `2025.acl-long.403.pdf`; su SHA-256 figura en
`published-values.json`.

Las doce cifras se transcribieron de **figura 1, paneles inferiores, p. 8235**.
Se muestran como porcentajes en el SVG editable, sin recalcular medias a partir
de los CSV de los autores. La orden posterior del usuario «no calcules nada,
todo del paper» sustituye la propuesta inicial de recalcular los datos del repositorio.
No se incorporan recuentos derivados ni intervalos de confianza reconstruidos.
La figura publica 0.637 para humanos/reflexivo/nonGP: se muestra **63,7 %**, no
63,8 %. La tabla 6 confirma los seis valores de Gemma-9B (no Gemma-9B-Inst).

| Condición | Humanos GP / nonGP | Gemma-2-9B GP / nonGP |
|---|---|---|
| Plausible | 0.133 / 0.198 | 0.149 / 0.224 |
| Implausible | 0.480 / 0.560 | 0.364 / 0.550 |
| Reflexive | 0.304 / 0.637 | 0.203 / 0.462 |

Ejemplo: §1, (1)–(2), p. 8235–8236. Condiciones: tabla 1, §2 y §3.1,
ejemplos (4)–(5). Procedimiento humano: §3.1. Procedimiento LLM: §4.1.
La traducción española es explicativa y no se presenta como material evaluado.
La composición y revelaciones son recursos de presentación, no un método experimental.

`python3 scripts/render_amouyal_chart.py` regenera el SVG y el inventario literal.
El script solo transcribe las cifras publicadas y dibuja las barras; no agrega datos.
`assets/revised/chart-18.svg` permanece como archivo histórico de la PPTX original,
sin aparecer en el bloque nuevo.
