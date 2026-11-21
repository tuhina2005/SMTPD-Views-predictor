Test-set metrics. Deep models: mean ± std over seeds. Δ = seed-matched difference (negative ΔAMAE / positive ΔASRC = better).

## Main results (random split, test set)

| setting                     | model                                  |   AMAE | ASRC   | seeds   |
|:----------------------------|:---------------------------------------|-------:|:-------|:--------|
| Without early views (no EP) | Paper (reported)                       |  1.562 | 0.856  | —       |
| Without early views (no EP) | Mean                                   |  3.492 | —      | —       |
| Without early views (no EP) | Ridge regression                       |  1.985 | 0.791  | —       |
| Without early views (no EP) | CatBoost                               |  1.658 | 0.849  | —       |
| Without early views (no EP) | Ours: ResNet, batch 64 (Mac check run) |  1.605 | 0.854  | 1       |
| With Day 1 views (EP)       | Paper (reported)                       |  0.717 | 0.959  | —       |
| With Day 1 views (EP)       | Mean                                   |  3.48  | —      | —       |
| With Day 1 views (EP)       | Persistence (Day 1 repeated)           |  2.275 | 0.952  | —       |
| With Day 1 views (EP)       | Ridge regression                       |  0.914 | 0.956  | —       |
| With Day 1 views (EP)       | CatBoost                               |  0.745 | 0.962  | —       |

## Unseen-channel split vs random split

| setting   | model    |   random_AMAE | channel_AMAE   |   random_ASRC | channel_ASRC   | AMAE_increase   |
|:----------|:---------|--------------:|:---------------|--------------:|:---------------|:----------------|
| no EP     | Ridge    |         1.985 | 2.031          |         0.791 | 0.761          | +0.046          |
| no EP     | CatBoost |         1.658 | —              |         0.849 | —              | —               |
| EP        | Ridge    |         0.914 | 0.921          |         0.956 | 0.952          | +0.007          |
| EP        | CatBoost |         0.745 | —              |         0.962 | —              | —               |

