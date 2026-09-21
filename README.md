# EarthTrend Detective Pro

**NASA Space Apps Challenge 2026**  
Challenge: **Be An Earth System Trend Detective!**  
Team: **decoder**

## Overview

EarthTrend Detective Pro is an evidence-first Earth system trend investigation tool. It helps users investigate long-term environmental changes using NASA Earth observation and climate data.

The project focuses on identifying trends, testing their statistical significance, examining spatial consistency, and presenting the evidence and limitations behind each result.

## What It Does

- Investigates environmental trends for a selected location
- Analyzes temperature, precipitation, and wind variables
- Builds annual observations from monthly NASA data
- Calculates Theil-Sen trend slopes
- Uses a modified Mann-Kendall significance test for autocorrelated data
- Performs a spatial comparison around the reference location
- Applies multiple-testing correction to spatial significance results
- Provides an evidence/reproducibility trail
- Separates environmental event context from long-term trend claims

## NASA Data

The project uses NASA POWER data for:

- Temperature
- Precipitation
- Wind speed

NASA POWER documentation:

https://power.larc.nasa.gov/

NASA Earthdata:

https://www.earthdata.nasa.gov/

## Scientific Method

The analysis uses complete calendar-year observations based on 12 valid monthly observations.

The reference climatology uses the 1991-2020 period where sufficient observations are available.

Trend estimation uses the Theil-Sen slope.

Trend significance is evaluated using a modified Mann-Kendall approach for autocorrelated annual observations when enough observations are available.

Spatial analysis uses a reference-centered grid and applies Benjamini-Yekutieli false discovery rate correction across valid cell-level tests.

Short records are treated as descriptive rather than being presented as statistically significant trends.

## Evidence Guardrails

The application explicitly avoids overclaiming:

- Trend does not mean causality.
- A point measurement does not represent an entire region.
- Non-significance does not mean no change.
- A wildfire event feed is contextual evidence, not a climate trend rate.
- Statistical results depend on the available record and data quality.

## Reproducibility

Evidence records include source information, retrieval metadata, coordinates, methodology information, and evidence hashes where available.

## Demo

See the 7-slide presentation:

`demo.pdf`

## Live Application

https://earth-trend-detective.base44.app/

## Source Code

https://github.com/takiibneduha3-ux/earthtrend-detective

## AI Disclosure

AI-assisted development was used during the creation of the project. AI assistance was used for development support, research assistance, documentation, and presentation preparation.

The scientific methodology, data sources, evidence boundaries, and project claims are explicitly documented rather than being presented as unsupported AI-generated conclusions.

## Team

Team: decoder

NASA Space Apps Challenge 2026

## License

See `LICENSE`.
