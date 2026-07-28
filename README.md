# Earthquake Analysis (1970-2014)

A comprehensive geospatial data analysis project examining earthquake patterns and characteristics over a 44-year period (1970-2014).

## Project Overview

This project analyzes historical earthquake data to identify patterns, trends, and geographical distributions of seismic events. The analysis combines geospatial visualization, statistical profiling, and data cleaning to provide insights into earthquake occurrence, magnitude, and depth characteristics.

## Dataset

- **Time Period**: 1970-2014
- **Main Data File**: `earthquakes1970-2014.csv`
- **Cleaned Data File**: `earthquakes1970-2013.csv_imp.csv`
- **Total Records**: Thousands of earthquake events with full metadata

## Project Structure

### Notebooks

1. **0.Data_Profiling&Cleaning.ipynb**
   - Data loading and exploration
   - Statistical profiling (describe, info, null values)
   - Data quality assessment
   - Feature engineering and data cleaning
   - Gap and distance distribution analysis

2. **1.EARTHQUAKE_ANALYSIS_1970-2014.ipynb**
   - Comprehensive earthquake analysis
   - Geospatial visualizations
   - Temporal trend analysis
   - Magnitude and depth correlations
   - Interactive maps and charts

## Dataset Columns

| Column | Type | Description |
|--------|------|-------------|
| **DateTime** | Temporal | Date and time of earthquake occurrence |
| **Latitude** | Geographic | North-South position (-90° to 90°) |
| **Longitude** | Geographic | East-West position (-180° to 180°) |
| **Depth** | Numeric | Depth in kilometers (0-700+ km) |
| **Magnitude** | Numeric | Energy release on logarithmic scale |
| **MagType** | Categorical | Type of magnitude scale used (Mw, Ms, Mb, Me, ML, Mc, Md, Unk) |
| **NbStations** | Numeric | Number of seismic stations that recorded the event |
| **Gap** | Numeric | Largest azimuthal gap in station distribution |
| **Distance** | Numeric | Distance to nearest seismic station (km) |
| **RMS** | Numeric | Root Mean Square of travel-time residuals |
| **Source** | Categorical | Seismic network/agency that reported the event |
| **EventID** | Identifier | Unique earthquake event identifier |

## Magnitude Scales

The project uses multiple magnitude scales to classify earthquakes:

- **Mw** (Moment Magnitude) - Modern standard; based on seismic moment
- **Ms** (Surface-wave Magnitude) - Based on surface wave amplitude
- **Mb** (Body-wave Magnitude) - Based on P-wave amplitude
- **Me** (Energy Magnitude) - Derived from radiated seismic energy
- **ML** (Local Magnitude/Richter Scale) - Used for small, local events
- **Mc** (Coda Magnitude) - Based on duration of seismic signal
- **Md** (Duration Magnitude) - Similar to Mc, based on signal length
- **Unk** (Unknown) - Magnitude type not specified

## Earthquake Depth Classification

- **Shallow**: 0-70 km - High amplitude surface waves
- **Intermediate**: 70-300 km - Complex P and S wave patterns
- **Deep**: 300-700+ km - Associated with sinking lithospheric slabs

## Technologies Used

- **Python** - Data analysis and processing
- **Pandas** - Data manipulation and analysis
- **GeoPandas** - Geospatial data handling
- **Matplotlib** - Statistical visualization
- **Plotly** - Interactive visualizations
- **Shapely** - Geometric operations
- **Jupyter Notebooks** - Interactive analysis environment

## Key Libraries

```python
import pandas as pd
import geopandas as gpd
import matplotlib.pyplot as plt
import plotly.graph_objects as go
from shapely.geometry import Point
import datetime as dt
```

## Getting Started

1. **Install Dependencies**
   ```bash
   pip install pandas geopandas matplotlib plotly shapely jupyter
   ```

2. **Run Analysis**
   - Start with `0.Data_Profiling&Cleaning.ipynb` for data exploration
   - Continue to `1.EARTHQUAKE_ANALYSIS_1970-2014.ipynb` for full analysis

3. **Explore Results**
   - View interactive maps and visualizations
   - Analyze temporal trends and patterns
   - Examine magnitude/depth relationships

## Analysis Highlights

- Geospatial distribution of seismic events worldwide
- Temporal patterns in earthquake frequency
- Magnitude and depth relationships
- Data quality metrics and reliability indicators
- Statistical summaries and distributions

## Files in This Directory

```
├── README.md                                    # This file
├── 0.Data_Profiling&Cleaning.ipynb             # Data exploration & cleaning
├── 1.EARTHQUAKE_ANALYSIS_1970-2014.ipynb       # Main analysis notebook
├── earthquakes1970-2014.csv                    # Raw earthquake data
├── earthquakes1970-2013.csv_imp.csv            # Cleaned/imputed data
├── .gitignore                                  # Git ignore rules
└── .git/                                       # Version control
```

## Notes

- Data profiling helps understand data quality and completeness
- NbStations indicates confidence in magnitude calculations
- Multiple magnitude scales reflect different measurement methodologies
- Geographical coordinates use WGS84 (EPSG:4326) projection

## Author

Kenneth C. Medes

## Purpose

Created for geospatial analysis and earthquake pattern research.

## License

This is Kaggle's public dataset and analysis project. 
Please refer to Kaggle's terms of use for data and code usage.

## LAST UPDATED

May 3, 2026
