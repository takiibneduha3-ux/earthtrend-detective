# Data Sources

## NASA POWER

The application uses NASA POWER monthly data for location-based Earth-system trend investigation.

Parameters used by the application:

- `T2M` — air temperature at 2 meters
- `PRECTOTCORR` — bias-corrected precipitation parameter as returned by NASA POWER
- `WS10M` — wind speed at 10 meters

Source: <https://power.larc.nasa.gov/>

The application preserves the requested coordinate and the coordinate returned/snapped by the source. Returned coordinates and source metadata are part of the evidence record.

### Retrieval behavior

- Requests are made server-side through application functions.
- Invalid coordinates and invalid year ranges are rejected.
- Missing, invalid, duplicate, or fill-value records are not converted to zero.
- Upstream failure is represented as an unavailable or partial result rather than fabricated data.
- Cached results are labelled as cached; refreshed results are labelled live.

### Resolution and limitations

NASA POWER is a gridded model/reanalysis-oriented source. A returned grid coordinate is not an exact satellite-pixel observation and nearby grid requests may represent the same effective source cell. The spatial view is therefore exploratory context, not independent regional proof.

## NASA EONET

The application may use NASA EONET for event context when queried and available.

Source: <https://eonet.gsfc.nasa.gov/>

EONET event context is kept separate from the long-term climate trend. An event found in EONET is not proof of causation, and an event not found is not proof that no event occurred.

## NASA FIRMS

The application has an optional FIRMS integration for fire-detection context. It requires the server-side `NASA_FIRMS_MAP_KEY` secret when enabled.

Source: <https://firms.modaps.eosdis.nasa.gov/>

FIRMS detections are contextual observations. An active-fire detection is not automatically a fire perimeter, burned area, emissions estimate, or causal climate explanation. If the key is not configured or the source is unavailable, the application reports that state explicitly.

## Attribution

NASA data sources are used for the NASA Space Apps Challenge project. Users should review the terms and attribution requirements of each source before redistribution or operational deployment.
