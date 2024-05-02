# AgriMateMN
![GitHub last commit](https://img.shields.io/github/last-commit/TzuYuMa/AgriMateMN?style=for-the-badge)

## Overview  
AgriMateMN provides AGDD (Growing Degree Days) data for the Last Minnesota Growing Season (May-Sep 2023), Soil Moisture data from July 2023 to April 2024, and ET (Evapotranspiration) information. Selecting the desire area to download data with CSV or PDF file, or you can find the [Data URLs for GeoJson](#data-urls-for-geojson) Utilizing GeoJSON format from APIs. This supports agricultural decision-making in Minnesota by facilitating the comparison of various models for accurate analysis.

## Objectives  
- Develop a system to calculate and map AGDD, ET, and soil moisture for Minnesota Corn Growers.
- Utilize local and cloud computing to automate data processing from collection through spatial visualization via ArcOnline.
- Ensure data accuracy and seamless integration of varied datasets within a PostgreSQL database.
- Maintain user-friendly access and support real-time updates.

## APP link

## Data URLs for GeoJson
- AGDD: 
  ```python
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_agdd_idw
  ```
  In the app, we offer data for the previous growing season, spanning from **April 2023 to September 2023**. We employed Inverse Distance Weighted (IDW) interpolation to extrapolate data from 153 observation sites across the entirety of Minnesota.

  Our [Accuracy Assessment.ipynb](https://github.com/TzuYuMa/Corn/blob/main/Final%20Project/Accuracy%20Assessment.ipynb) concluded that IDW provided the most dependable results.
- ET: [ET Data URL]
- Soil Moisture:
  ```python
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_soil_moisture_<date>
  ```
  Please manually replace `<date>` with the desired year and month in your browser's address bar


  Available date range: 20237-20244 (July 2023 - April 2024)

  For example:
  
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_soil_moisture_20237
## Data Sources 
- **IEM**: Daily Min/Max temperature data.
- **NASA SMAP**: Soil Moisture.
- **TerraClimate**: Actual Evapotranspiration.
  
## Contributors 
- Tzu-Yu Ma  
- Samikshya Subedi
