Perovskite-Solar-Cell-Materials

Machine-learning framework for screening perovskite compositions and processing recipes — surrogate modeling (LightGBM ensemble) + uncertainty-aware NSGA-II multi-objective optimization.

Overview

Perovskite solar cells (PSCs) achieve very high power-conversion efficiencies (PCE) but are often limited by poor operational stability. This repository implements a reproducible pipeline that:

Trains LightGBM surrogates on a curated perovskite descriptor database to predict PCE and T80 (time to 80% of initial efficiency).

Uses an ensemble of LightGBM models to approximate predictive uncertainty.

Drives an NSGA-II multi-objective optimizer to obtain Pareto fronts that trade off efficiency vs. durability as a function of composition and processing variables.

Prioritizes robust, experimentally testable recipes by incorporating uncertainty into candidate selection.

Key reported results (example)

PCE prediction — R² = 0.9665, RMSE = 1.166, MAE = 0.553 (on held-out test set using the curated descriptor database).
