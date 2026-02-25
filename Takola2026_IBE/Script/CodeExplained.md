<details>
<summary>1) Setup and data preparation</summary>
<li> Load required packages </li> <li> Read SSF dataset and keep original copy </li> <li> Drop geometry for non-spatial modeling </li> <li> Remove rare crop types (keep crop types with ≥ 31 obs) </li>
</ul>
<details>
<details>
<summary>2) Fit SSF models by ecological domain (GLMMs with individual-level random slopes)</summary>
<li> Fit food resources model (binomial SSF) </li> <li> Extract food fixed effects </li> <li> Extract food random slope BLUPs (ETF, SWI, ETF×SWI) </li> <li> Fit weather model (temp, precipitation, wind) </li> <li> Extract weather fixed effects </li> <li> Extract weather random slope BLUPs (temperature) </li> <li> Fit soil model (SWI, nitrogen, organic carbon + step-level RE) </li> <li> Extract soil fixed effects </li> <li> Extract soil random slope BLUPs (SWI, N, orgC) </li> <li> Fit human activity model (pop dens, THP, crop intensity, pesticides) </li> <li> Extract human activity fixed effects </li> <li> Extract human activity random slope BLUPs (pop dens, THP, glyphosate, propiconazole) </li> <li> Fit vegetation model (NDVI, crop type, pesticides) </li> <li> Extract vegetation fixed effects </li> <li> Extract vegetation random slope BLUPs (NDVI, glyphosate, propiconazole) </li>
<details>
<details>
<summary>3) Combine and visualize fixed effects across domains</summary>
<li> Bind fixed effects from all models into one table </li> <li> Clean labels and set facet order </li> <li> Export fixed effects table </li> <li> Plot coefficient estimates with 95% CI by domain </li>
<details>
<details>
<summary>4) Build and plot individual reaction norm lines from random slopes</summary>
<li> Define helpers to extract fixed slopes and build per-id lines </li> <li> Create x-grids for predictors (and interaction product grid) </li> <li> Build reaction norm datasets by domain </li> <li> Export one CSV per domain of reaction norm lines </li> <li> Plot per-domain reaction norms (lines by individual; facets by predictor) </li>
<details>
<details>
  <summary>5) Compute relative selection probability (RSP) per model and join to the dataset</summary>
  <ul>
    <li>Add unique row id for safe joins</li>
    <li>Store fitted models in a named list</li>
    <li>Predict linear predictor for each model and compute RSP = exp(eta)</li>
    <li>Scale RSP within each individual and domain</li>
    <li>Pivot to wide and join back to main data</li>
    <li>Export dataset with per-domain RSP columns</li>
  </ul>
</details>

<details>
  <summary>6) Filter to core points using scaled RSP and visualize predictor-space structure</summary>
  <ul>
    <li>Define threshold and identify scaled RSP columns</li>
    <li>Filter rows where any domain exceeds threshold</li>
    <li>Define predictor sets per domain</li>
    <li>Build convex hulls per individual for each predictor pair facet</li>
    <li>Create and display one pairs+hulls plot per domain</li>
  </ul>
</details>

<details>
  <summary>7) Create a combined RSP_scaled index across domains for niche analyses</summary>
  <ul>
    <li>Compute row-wise maximum scaled RSP across domains</li>
  </ul>
</details>

<details>
  <summary>8) Niche overlap and niche breadth per domain (PCA → convex hull → Jaccard)</summary>
  <ul>
    <li>Define function to build realized/potential polygons in PCA space</li>
    <li>Define function to compute pairwise Jaccard overlap from polygons</li>
    <li>Set core potential fraction (optional) for available steps</li>
    <li>For each domain build polygons per id for realized and potential niches</li>
    <li>Compute overlap tables (Realized + Potential)</li>
    <li>Compute breadth tables (polygon areas)</li>
    <li>Export overlap and breadth results</li>
    <li>Plot overlap heatmaps by domain and niche type</li>
    <li>Plot breadth comparisons by id within domain</li>
  </ul>
</details>

<details>
  <summary>9) Repeatability per domain and niche type (rptR) on core data</summary>
  <ul>
    <li>Define robust extractor for repeatability estimate and CI</li>
    <li>Define repeatability runner across variables</li>
    <li>Filter to core niche rows again (any scaled RSP &gt; thr)</li>
    <li>Compute repeatability for Realized and Potential per domain</li>
    <li>Export repeatability table</li>
    <li>Run diagnostics (estimate outside CI)</li>
    <li>Plot repeatabilities (points + CI) per domain</li>
  </ul>
</details>
