# Data

Analysis outputs exported from the water productivity pipeline.
All values reflect **active pivot-seasons only**.
Inactive pivot-seasons are masked to prevent bare-soil evaporation
from contaminating water productivity and demand figures.

| File | Rows | What it contains |
|---|---|---|
| `seasonal_performance_summary.csv` | 4 | One row per season — area, demand, and mean WPb |
| `pivot_operational_classification.csv` | 166 | One row per pivot — class, average WPb, trend slope, coordinates |
| `master_seasonal_statistics.csv` | 664 | One row per pivot per season — all extracted variables |
| `master_dekadal_phenology.csv` | ~5,742 | One row per active pivot per 10-day period |
| `pivot_cwp_wide_trend.csv` | 166 | One column per season — WPb per pivot (inactive = NaN) |
| `season_windows.csv` | 4 | Irrigation season start, end, length, and peak water demand dekad |

**Data sources used in this pipeline:**

- FAO WaPOR v3 L3 — AETI and NPP at 20m resolution (10-day dekadal)
- FAO WaPOR PCP Level 1 — Precipitation at native ~5km resolution,
  resampled and aligned to the 20m AETI grid before analysis
- Sentinel-2 Level-2A — SAVI composites accessed via AWS Element84 STAC

Raw WaPOR raster files (.nc cubes) are not included due to file size.
