# Scientific Methodology

## Scope

The application investigates what is changing, where it is changing, how much it is changing, and whether the selected statistical test detects significant evidence of a monotonic trend. This is not a claim of causal attribution.

## Data quality gate

Monthly records are validated before analysis. Missing values, fill values, invalid numbers, and duplicate records are not silently converted to zero or interpolated. An annual observation is eligible only when all twelve calendar months are valid. Rejected years and exclusion reasons are retained in the evidence trail.

## Aggregation

Aggregation is parameter-specific and uses the source unit and semantics returned by NASA POWER. Temperature and wind use documented annual summaries. Precipitation is kept distinct from temperature and wind semantics and must not be described as an annual total unless the implemented aggregation supports that interpretation.

## Baseline and anomalies

The reference climatology is 1991–2020. Monthly climatology is calculated separately by calendar month when sufficient observations are available. Anomaly results are expressed relative to that reference period and preserve unavailable gaps.

## Trend magnitude

Theil–Sen slope is used as a robust monotonic trend summary. Pairwise slopes use actual calendar-year differences rather than sequence indexes. The result reports the slope, unit per year, valid record length, and limitations.

## Statistical significance

The application reports a two-sided autocorrelation-aware modified Mann–Kendall result using the Hamed–Rao method as documented in the application QA report. The alpha level is 0.05. Records below the implemented minimum are descriptive only and do not receive an inferential significance claim.

A non-significant result means that no statistically significant trend was detected under the selected test; it does not prove that no trend exists.

## Spatial analysis

A 5×5 reference-centred exploratory grid is used where spatial analysis is available. Returned source coordinates, failed cells, duplicate/effective cells, raw p-values, adjusted p-values, and the correction method are retained where available.

Grid cells are not assumed to be independent satellite pixels. Spatial output is contextual evidence and should not be read as independent regional confirmation.

## Event context and interpretation

EONET/FIRMS event context is separate from the long-term trend calculation. Association is not causation. Missing event context is not proof of no event, and an event record is not proof that the climate trend caused the event.

## Reproducibility

Evidence records include source metadata, retrieval time, requested and returned coordinates, methodology information, and hashes where available.

## Method and software versions

The Builder QA report identified the methodology as:

- Theil–Sen median pairwise slope
- Hamed–Rao modified Mann–Kendall, Hamed & Rao (1998)
- Baseline: 1991–2020
- Minimum baseline coverage: 24 valid years per calendar month
- Alpha: 0.05

The reported methodology version was not incremented during the final QA pass because no scientific method was changed. Verify the live application's displayed version before making a final submission claim.

## Limitations

NASA POWER meteorological variables are model/reanalysis-derived products and should be interpreted according to NASA POWER documentation and the limitations of the underlying datasets. A returned grid coordinate is not an exact satellite-pixel observation, nearby requests may represent the same effective source cell, monthly data cannot establish daily event impact, and non-significance does not prove that no environmental change exists.
