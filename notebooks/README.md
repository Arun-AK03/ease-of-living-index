# notebooks

Visualisation notebooks that read the finished outputs in `Data/processed/` and
`src/ranking/index dataset/` and produce the charts saved under `reports/`
(several correspond to figures in the paper). These sit on top of the pipeline —
they consume its results rather than building the index.

## Notebooks

| Notebook | Produces |
|---|---|
| `Econ_Visualisation.ipynb` | Economic sub-index plots (GDP growth, cost of living, KDE, index values) |
| `Institutional_Visualisation.ipynb` | Institutional sub-index plots (freedom of speech, institutional index) |
| `Quality of life_Visualisation.ipynb` | Quality-of-life plots (crime index, imputed distributions, QoL index) |
| `Sus_Visualisation.ipynb` | Sustainability plots (greenhouse emissions, imputed distributions) |
| `Ranking_Visualisation.ipynb` | Final ranking / composite Ease of Living Index plots, heatmaps, violin plots |
| `Visualisation_Fig 5.ipynb` | A specific paper figure (Fig 5) |
| `Visualisation.ipynb` | Empty / scratch placeholder |

## Notes
- Outputs land in `reports/` (and its per-pillar subfolders).
- `Visualisation.ipynb` is currently empty.
- Run the pipeline first (or use the shipped `Data/processed/` files) so the
  inputs these notebooks read already exist.
