Here's the updated README file, better aligned with the assignment prompt:

---

# WeatherPy & VacationPy - API Challenge

This repository contains two Jupyter notebooks that showcase the use of APIs to analyze weather data and plan vacations based on weather conditions, as part of the Python API Challenge. The challenge addresses the fundamental question: *"What is the weather like as we approach the equator?"* The goal is to analyze weather data across cities at varying latitudes to identify patterns and relationships between weather variables and proximity to the equator.

### Notebooks Overview:

1. **[WeatherPy.ipynb](https://github.com/JeanR41/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)**:  
   This notebook uses the OpenWeatherMap API to retrieve weather data from over 500 cities located at various latitudes. It visualizes relationships between latitude and weather variables such as temperature, humidity, cloudiness, and wind speed. The notebook also computes linear regression to explore the correlation between these weather variables and latitude in both the Northern and Southern Hemispheres.

2. **[VacationPy.ipynb](https://github.com/JeanR41/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)**:  
   Building on the weather data from the WeatherPy notebook, VacationPy helps plan vacation destinations based on ideal weather conditions. It uses the Geoapify API to find cities with perfect weather (e.g., temperature, wind speed, and humidity) and visualizes these locations on a map. The notebook also recommends nearby hotels for potential vacation spots.

### Part 1: WeatherPy Analysis

The **WeatherPy** notebook explores how weather conditions change with latitude. By visualizing key weather variables and applying linear regression models, the notebook identifies relationships between weather conditions (temperature, humidity, cloudiness, and wind speed) and latitude, answering the core question: *How does weather change as we approach the equator?*

#### Key Visualizations:

- **Latitude vs. Temperature**  
- **Latitude vs. Humidity**  
- **Latitude vs. Cloudiness**  
- **Latitude vs. Wind Speed**

#### Linear Regression Results:

- **Temperature vs. Latitude**:
  - **Northern Hemisphere**: Strong negative correlation (r² = -0.88) – as latitude increases, temperature decreases.
  - **Southern Hemisphere**: Weak positive correlation (r² = 0.18) – temperatures are slightly warmer near the equator, but the correlation is not as strong as in the Northern Hemisphere.

- **Humidity vs. Latitude**:
  - **Northern Hemisphere**: Moderate positive correlation (r² = 0.44) – humidity tends to increase closer to the equator.
  - **Southern Hemisphere**: Strong positive correlation (r² = 0.76) – there is a notable trend of higher humidity near the equator, influenced by regional factors.

- **Cloudiness vs. Latitude**:
  - **Northern Hemisphere**: Weak correlation (r² = 0.15) – cloudiness does not show a strong relationship with latitude, suggesting other factors influence cloud cover.
  - **Southern Hemisphere**: Moderate positive correlation (r² = 0.63) – cloudiness is more strongly linked to latitude, potentially influenced by the Intertropical Convergence Zone (ITCZ).

- **Wind Speed vs. Latitude**:
  - **Northern Hemisphere**: Weak negative correlation (r² = -0.24) – wind speed is not strongly influenced by latitude, with other factors playing a role.
  - **Southern Hemisphere**: Moderate negative correlation (r² = -0.54) – wind speeds increase as latitude moves away from the equator, potentially due to larger atmospheric circulation patterns.

#### Discussion:
The linear regression plots illustrate how weather variables like temperature, humidity, cloudiness, and wind speed correlate with latitude. In the Northern Hemisphere, the relationships are clearer, especially for temperature and humidity, while the Southern Hemisphere shows more variation, especially for cloudiness and wind speed.

### Part 2: VacationPy

The **VacationPy** notebook builds on the insights from WeatherPy to help plan vacations based on ideal weather conditions. By filtering cities based on factors like temperature, wind speed, and cloudiness, the notebook suggests destinations with the perfect weather for a vacation.

#### Key Tasks:

- **Map Visualization**: Display cities on a map, with the size of each point representing humidity.
- **Ideal Weather Filter**: Narrow down the list of cities based on ideal weather criteria (e.g., temperature between 24-38°C, and less than 80% cloudiness).
- **Hotel Recommendations**: For each city, use the Geoapify API to recommend hotels located within 10,000 meters of the city center, and add hotel information to the map.

This notebook helps users visualize potential vacation spots that align with their desired weather conditions, making vacation planning both informative and interactive.

### Requirements:
- Python 3.x
- Jupyter Notebook or JupyterLab
- Libraries:
  - Pandas
  - Requests
  - Matplotlib
  - GeoPandas
  - Google Maps API
  - OpenWeatherMap API
  - Geoapify API
  - Scipy
  - geoViews

### Getting Started:
1. Clone or download the repository.
2. Install the necessary libraries using pip or conda.
3. Obtain API keys for OpenWeatherMap and Geoapify and place them in the `api_keys.py` file.
4. Run the **WeatherPy.ipynb** notebook to analyze weather data across cities and create the visualizations.
5. Run the **VacationPy.ipynb** notebook to plan your ideal vacation and view recommendations on a map.
