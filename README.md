# Chhattisgarh Climate Analysis

A comprehensive climate change analysis project focusing on temperature and rainfall patterns in Chhattisgarh, India, spanning from 1951 to 2024 (74 years). This repository contains data collection, analysis, and visualization notebooks for four key locations in the state.

## 📍 Locations Analyzed

1. **Raipur** (Lat: 21.26°N, Lon: 81.64°E) - Capital city of Chhattisgarh
2. **Korba** (Lat: 21.35°N, Lon: 82.73°E) - Industrial city
3. **Bastar** (Lat: 19.81°N, Lon: 81.93°E) - Southern district
4. **Ambikapur** (Lat: 23.12°N, Lon: 83.19°E) - Northern city

## 📊 Data Source

- **India Meteorological Department (IMD)** data accessed via `imdlib`
- **Time Period**: 1951-2024 (74 years of daily observations)
- **Variables**: 
  - `tmin`: Daily minimum temperature (°C)
  - `tmax`: Daily maximum temperature (°C)
  - `rain`: Daily rainfall (mm)

## 📁 Repository Structure

```
Chhattisgarh/
│
├── Data_collection.ipynb           # Data collection and preprocessing notebook
├── Raipur.ipynb                    # Comprehensive climate analysis for Raipur
├── Raipur_extreme.ipynb            # Extreme events analysis for Raipur
├── Korba_extreme.ipynb             # Extreme events analysis for Korba
├── Ambikapur_extreme.ipynb         # Extreme events analysis for Ambikapur
├── Bastar_extreme.ipynb            # Extreme events analysis for Bastar
│
├── Raipur.csv                      # Processed climate data for Raipur
├── Korba.csv                       # Processed climate data for Korba
├── Ambikapur.csv                   # Processed climate data for Ambikapur
├── Bastar.csv                      # Processed climate data for Bastar
│
└── README.md                       # This file
```

## 🔬 Analysis Components

### 1. Data Collection (`Data_collection.ipynb`)
- Downloads IMD gridded climate data using `imdlib`
- Extracts data for specific coordinates
- Processes and saves data to CSV files for each location

### 2. Comprehensive Analysis (`Raipur.ipynb`)
Comprehensive climate analysis including:

#### Basic Statistics
- Descriptive statistics for temperature and rainfall
- Distribution analysis (boxplots, histograms)
- Time series visualization

#### Temperature Analysis
- **Monthly Heatmaps**: Min, mean, and max temperature patterns across years
- **Annual Trends**: Linear regression analysis for temperature trends
- **Temperature Difference**: Analysis of diurnal temperature range (tmax - tmin)

#### Rainfall Analysis
- Monthly and annual rainfall patterns
- Time series analysis
- Trend analysis using linear regression

#### Forecasting
- **Prophet Model**: Temperature and rainfall forecasting (10 years ahead)
- Future trend projections

### 3. Extreme Events Analysis (`*_extreme.ipynb`)
Analysis of extreme climate events for each location:

#### Temperature Extremes
- **Cold Days**: Annual count of days with tmin < 10°C
- **Hot Days**: Annual count of days with tmax > 40°C
- Trend analysis for extreme temperature events
- Year-to-year comparison (1951 vs 2024, early vs recent decades)

#### Rainfall Extremes
- **Heavy Rainfall Days**: Annual count of days with rain > 140 mm
- **Moderate Rainfall Days**: Days with rain between 1-60 mm
- Trend analysis for extreme rainfall events
- Seasonal comparison across different years

## 🛠️ Requirements

### Python Packages
```bash
pip install imdlib
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install prophet
pip install geopandas
```

### Key Dependencies
- `imdlib`: For accessing IMD climate data
- `pandas`: Data manipulation and analysis
- `numpy`: Numerical operations
- `matplotlib`: Basic plotting
- `seaborn`: Advanced visualization
- `prophet`: Time series forecasting (Facebook/Meta)
- `geopandas`: Geospatial data handling (for data collection)

## 🚀 Usage

### 1. Data Collection
Run `Data_collection.ipynb` to:
- Download IMD data (requires internet connection)
- Extract data for specific coordinates
- Generate CSV files for analysis

**Note**: Ensure you have the required directory structure for storing IMD data files.

### 2. Climate Analysis
Run `Raipur.ipynb` for comprehensive analysis:
- Load the CSV data
- Execute cells sequentially
- Generate visualizations and forecasts

### 3. Extreme Events Analysis
Run location-specific extreme events notebooks:
- `Raipur_extreme.ipynb`
- `Korba_extreme.ipynb`
- `Ambikapur_extreme.ipynb`
- `Bastar_extreme.ipynb`

Each notebook can be run independently using the corresponding CSV file.

## 📈 Key Findings (Example: Raipur)

### Temperature Trends
- **Maximum Temperature**: Slight increasing trend (slope ≈ 0.0106°C/year)
- **Minimum Temperature**: Very small increasing trend (slope ≈ 0.0014°C/year)
- **Hot Days (>40°C)**: Increasing trend (slope ≈ 0.06 days/year)
- **Cold Days (<10°C)**: Decreasing trend (slope ≈ -0.02 days/year)

### Rainfall Trends
- **Annual Rainfall**: Slight decreasing trend (slope ≈ -2.40 mm/year)
- High interannual variability
- Monsoon-driven seasonal patterns

### Extreme Events
- Increasing frequency of extreme hot days
- Decreasing frequency of extreme cold days
- Variable patterns in heavy rainfall events

## 📊 Visualizations

The notebooks generate various visualizations including:
- Time series plots
- Monthly/annual heatmaps
- Boxplots and histograms
- Scatter plots with trend lines
- Year-to-year comparisons
- Forecast plots

## 🔍 Methodology

1. **Data Processing**: IMD gridded data extraction for specific coordinates
2. **Trend Analysis**: Linear regression for identifying long-term trends
3. **Extreme Events**: Threshold-based counting and trend analysis
4. **Forecasting**: Prophet time series model for future projections
5. **Visualization**: Comprehensive plots for pattern identification

## 📝 Notes

- Data spans 74 years (1951-2024) with daily resolution
- Missing values are handled during data processing
- Trend analysis uses linear regression; results should be interpreted with statistical significance testing
- Forecasting models (Prophet) provide projections but should be validated
- Location-specific analyses may show different patterns due to regional climate variations

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📄 License

This project is open source and available for research and educational purposes.

## 🙏 Acknowledgments

- **India Meteorological Department (IMD)** get climate data
- **imdlib** library developers for data access tools
- Climate research community for methodology and insights

## 📧 Contact

For questions or suggestions, please open an issue in the repository.

**Last Updated**: 2025
**Data Period**: 1951-2024
**Analysis Type**: Climate Change & Extreme Events

