# Data

Five ERA5 monthly-mean NetCDF files covering January 1998 to December 2024 over the Indian region (7°N to 37°N, 68°E to 98°E, 0.25° grid, 121 x 121 points, 324 monthly steps).

| File | Variable name in file | Description | Units |
|---|---|---|---|
| `windspeed.nc` | `ws` | 10 m wind speed, computed from u10 and v10 with CDO | m/s |
| `temperature.nc` | `t2m` | 2 m temperature | K |
| `rainfall.nc` | `tp` | Total precipitation | m |
| `pressure.nc` | `msl` | Mean sea-level pressure | Pa |
| `humidity.nc` | `rh` | Relative humidity | % |

## Source

ERA5 reanalysis (Hersbach et al., 2020), Copernicus Climate Change Service (C3S) Climate Data Store: https://cds.climate.copernicus.eu/

*Contains modified Copernicus Climate Change Service information.*

## Usage

The files are loaded and aligned by the `build_dataset` function in the notebook, which snaps timestamps to month start and merges the five files on their common months.

Reference: Hersbach, H., et al. (2020). The ERA5 global reanalysis. *Quarterly Journal of the Royal Meteorological Society*, 146, 1999-2049.
