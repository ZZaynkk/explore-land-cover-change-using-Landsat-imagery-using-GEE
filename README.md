# explore-land-cover-change-using-Landsat-imagery-using-GEE
Google Earth Engine analysis of land-cover change in the Toshka–Lake Nasser region, Egypt (2013–2024), using Landsat 8, NDVI and MNDWI for classification, area statistics and change detection.

## Research question

How did vegetation, water and other land cover change across the
study area between 2013 and 2024?

## Project files

- `src/land_cover_change.js`: complete Earth Engine analysis.
- `results/land_cover_area_km2.csv`: recorded area statistics.
- `results/transitions_2013_2024_km2.csv`: recorded transition areas.

## How to run

1. Open https://code.earthengine.google.com/
2. Sign in with an Earth Engine-enabled account.
3. Copy `src/land_cover_change.js` into a new script.
4. Click Run.
5. Use Layers to view maps and Console to inspect statistics.

This program runs in Google Earth Engine, not directly on GitHub
or in Node.js. No npm packages are required.

## Study area

Toshka–Lake Nasser region, southern Egypt.

Bounding coordinates:
- West: 31.03790606
- South: 22.46568687
- East: 32.3617586
- North: 23.36880901

## Data and preprocessing

- Dataset: LANDSAT/LC08/C02/T1_TOA
- Years: 2013, 2018, 2019, 2024
- Period: April–December in each year
- Scene cloud cover: less than 20%
- QA_PIXEL bits 0–5 masked
- Saturated pixels masked using QA_RADSAT
- Median spectral composite for each year

## Spectral indices

NDVI = (B5 - B4) / (B5 + B4)

MNDWI = (B3 - B6) / (B3 + B6)

Indices are calculated from the median spectral composite.

## Preliminary classification

| Code | Class | Rule |
| --- | --- | --- |
| 0 | Other | Remaining valid pixels |
| 1 | Vegetation | NDVI > 0.2 and not water |
| 2 | Water | MNDWI > 0 |

Water takes priority.

## Area and change detection

Statistics use pixels valid in all four years.

Pixel areas are summed at 30 m resolution using EPSG:32636.
Areas are reported in square kilometres.

Post-classification comparison uses:

transition = class_2013 × 3 + class_2024

Six transitions between different classes are reported.

## Recorded results

The CSV files contain previously recorded project outputs.
They were not regenerated during project packaging.

Between 2013 and 2024:
- Vegetation increased by approximately 529.749 km².
- Water increased by approximately 850.364 km².
- Other land cover decreased by approximately 1380.113 km².

## Limitations

This is preliminary threshold-based classification.
No independent accuracy assessment was performed.

Vegetation does not represent all farmland.
Other is a residual category, not exclusively bare land.
Coverage_percent measures valid spatial coverage, not accuracy.

Seasonality, compositing and threshold selection can affect results.
The analysis alone does not establish the causes of observed changes.

## Validation

The main script passed JavaScript syntax checking.
Earth Engine execution was not repeated during packaging.
