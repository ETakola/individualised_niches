<details>
<summary>1) Setup and data preparation</summary>
<ul><li>Load required packages 
  >`library(...)` </li> 
  <li>Read SSF dataset and keep original copy 
    >`ssf_dat_sfc10k <- readRDS(...)`, `ssf_dat_sfc10k_orig <- ssf_dat_sfc10k` </li> 
    <li>Drop geometry for non-spatial modeling | `ssf_dat_sfc10k_no_geom <- sf::st_drop_geometry(ssf_dat_sfc10k)` </li> 
      <li>Remove rare crop types (keep crop types with ≥ 31 obs) | `filter(crop_type %in% names(table(crop_type))[table(crop_type) >= 31])` </li><ul>
