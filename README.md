# NYC Transit vs. Weather

## Overview

This project explores how weather conditions influence transportation patterns across New York City's five boroughs. By combining weather data with public transit ridership, vehicle traffic, and bridge/tunnel traffic, we investigate how precipitation, snowfall, and seasonal patterns relate to commuting behavior.

The project uses a Python-based ETL pipeline to collect, clean, transform, and combine multiple datasets into an hourly dataset for analysis and visualization in Tableau.

## Project Objectives

- Analyze how rain and precipitation affect subway and bus ridership.
- Examine how snowfall relates to vehicle traffic and transportation disruptions.
- Compare transportation patterns across the five boroughs.
- Identify boroughs that may benefit most from infrastructure improvements.
- Explore ridership and traffic trends to support congestion pricing and transportation planning.
- Analyze hourly ridership patterns to explore transportation-related NYPD deployment.

## Key Findings

- **Rain and transit ridership:** Subway and bus ridership generally decrease as precipitation increases.
- **Snow and road traffic:** Snow events are associated with changes in vehicle traffic, highlighting the importance of snow removal and road maintenance.
- **Borough differences:** Each borough has different transportation needs based on its reliance on subways, buses, cars, and bridges.
- **Infrastructure needs:** Boroughs with limited subway access and higher bus dependency may be more vulnerable to weather-related disruptions.
- **Ridership patterns:** Hourly transit patterns vary across boroughs, which can help inform planning and resource allocation.

## Data Pipeline

The project uses an ETL (Extract, Transform, Load) pipeline developed in Python.

### 1. Extract
Data is collected from multiple public data sources, including weather APIs and NYC transportation datasets.

### 2. Transform
The datasets are processed using Pandas. This includes cleaning data, standardizing borough names, converting timestamps, aggregating hourly records, and preparing datasets for integration.

### 3. Load
Processed datasets are loaded into a Supabase-hosted PostgreSQL database. Separate tables are created for each data source before being joined into a master hourly dataset.

### Pipeline Structure

- `weather_hourly` — hourly weather conditions
- `subway_hourly` — hourly subway ridership by borough
- `bus_hourly` — hourly bus ridership by borough
- `bridges_tunnels_hourly` — hourly bridge and tunnel traffic
- `traffic_volume_hourly` — street traffic counts and sensor counts
- `master_hourly` — combined dataset used for analysis

## Data Sources

- [Open-Meteo](https://open-meteo.com/) — historical weather data
- [NYC Open Data](https://opendata.cityofnewyork.us/) — automated traffic volume counts
- [MTA Data](https://data.ny.gov/) — subway, bus, and bridge/tunnel transportation data

## Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **SQL**
- **PostgreSQL**
- **Supabase**
- **REST APIs**
- **Jupyter Notebook / Google Colab**
- **Tableau**

## Tableau Dashboards

### Weather vs. Transit

Explore how precipitation and weather conditions relate to MTA ridership across NYC boroughs.

[View Weather vs. Transit Dashboard](https://public.tableau.com/views/WeathervsTransit/WeatherImpactonMTARidership?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Ridership Forecast

Explore historical ridership trends and forecasted transit patterns.

[View Ridership Forecast Dashboard](https://public.tableau.com/views/5000_data_sheng_dash/ForecastDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Recommendations

Based on our analysis, we explored several potential improvements:

- Improve weather protection at bus stops in bus-dependent areas.
- Prioritize road, bridge, and tunnel maintenance during severe weather.
- Consider transportation infrastructure differences when planning investments.
- Use ridership trends to inform congestion management and transportation planning.
- Evaluate transit demand patterns when planning public safety resource allocation.

## Team 5000

- Akram Uddin
- Abdul Muswara
- Tanvir Islam
- Hirwa Divin Iradukunda
- Rawnak Ahmed
- Diego Ordonez

