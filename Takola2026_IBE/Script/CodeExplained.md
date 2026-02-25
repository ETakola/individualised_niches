<details>
<summary>1) Setup and data preparation</summary>
<li> Load required packages </li> <li> Read SSF dataset and keep original copy </li> <li> Drop geometry for non-spatial modeling </li> <li> Remove rare crop types (keep crop types with ≥ 31 obs) </li>

<summary>2) Fit SSF models by ecological domain (GLMMs with individual-level random slopes)</summary>
<li> Fit food resources model (binomial SSF) </li> <li> Extract food fixed effects </li> <li> Extract food random slope BLUPs (ETF, SWI, ETF×SWI) </li> <li> Fit weather model (temp, precipitation, wind) </li> <li> Extract weather fixed effects </li> <li> Extract weather random slope BLUPs (temperature) </li> <li> Fit soil model (SWI, nitrogen, organic carbon + step-level RE) </li> <li> Extract soil fixed effects </li> <li> Extract soil random slope BLUPs (SWI, N, orgC) </li> <li> Fit human activity model (pop dens, THP, crop intensity, pesticides) </li> <li> Extract human activity fixed effects </li> <li> Extract human activity random slope BLUPs (pop dens, THP, glyphosate, propiconazole) </li> <li> Fit vegetation model (NDVI, crop type, pesticides) </li> <li> Extract vegetation fixed effects </li> <li> Extract vegetation random slope BLUPs (NDVI, glyphosate, propiconazole) </li>

<summary>3) Combine and visualize fixed effects across domains</summary>
<li> Bind fixed effects from all models into one table </li> <li> Clean labels and set facet order </li> <li> Export fixed effects table </li> <li> Plot coefficient estimates with 95% CI by domain </li>

<summary>4) Build and plot individual reaction norm lines from random slopes</summary>
<li> Define helpers to extract fixed slopes and build per-id lines </li> <li> Create x-grids for predictors (and interaction product grid) </li> <li> Build reaction norm datasets by domain </li> <li> Export one CSV per domain of reaction norm lines </li> <li> Plot per-domain reaction norms (lines by individual; facets by predictor) </li>
