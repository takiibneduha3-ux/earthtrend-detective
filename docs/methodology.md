# Scientific Methodology

## Data

EarthTrend Detective Pro uses NASA POWER monthly data for temperature, precipitation, and wind variables.

## Annualization

An annual observation is calculated only when all 12 calendar months are valid.

The annual value is the arithmetic mean of the 12 monthly values.

## Baseline

The reference climatology uses 1991-2020 where sufficient annual observations are available.

## Trend

Theil-Sen slope is used as the robust trend estimator.

The slope uses actual calendar-year gaps between observations.

## Significance

A modified Mann-Kendall procedure is used for autocorrelated annual observations when at least 8 complete annual observations are available.

Shorter records are reported descriptively and are not presented as statistically significant trends.

## Spatial Analysis

A 5x5 reference-centered spatial sweep is used to examine whether a detected point trend is spatially consistent.

Valid cell-level significance tests are adjusted using the Benjamini-Yekutieli false discovery rate procedure at q=0.05.

## Interpretation

The application distinguishes:

1. Observed trend
2. Statistical significance
3. Spatial consistency
4. Event context
5. Interpretation limitations

The system does not infer causality from correlation or temporal overlap.

## Reproducibility

Evidence records include source metadata, retrieval time, coordinates, methodology information, and hashes where available.

## Limitations

NASA POWER meteorological variables are model/reanalysis-derived products and should be interpreted according to NASA POWER documentation and the limitations of the underlying datasets.

A statistically non-significant result does not prove that no environmental change exists.
