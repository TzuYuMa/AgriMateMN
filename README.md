# AgriMateMN APP
![GitHub last commit](https://img.shields.io/github/last-commit/TzuYuMa/AgriMateMN?style=for-the-badge)

## Overview  
AgriMateMN provides AGDD (Growing Degree Days) data for the Last Minnesota Growing Season (May-Sep 2023), Soil Moisture data from July 2023 to April 2024, and ET (Evapotranspiration) information. Selecting the desire area to download data with CSV or PDF file, or you can find the [Data URLs for GeoJson](#data-urls-for-geojson) Utilizing GeoJSON format from APIs. This supports agricultural decision-making in Minnesota by facilitating the comparison of various models for accurate analysis.

## APP link

## Data URLs for GeoJson
### AGDD Data
- **Download for Entire State of Minnesota:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_agdd_minnesota
  ```

- **Download by County:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_agdd_<county>
  ```
  *(Replace `<county>` with the desired county name (lower case, spaces replaced with '_'))*

  For example:
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_agdd_st_louis
  ```

  *Data Coverage: Previous growing season, spanning from April 2023 to September 2023. Utilizes Inverse Distance Weighted (IDW) interpolation based on 153 observation sites across Minnesota.*

### ET Data
- **ET Data URL**: [ET Data URL]

### Soil Moisture Data
- **Download for Entire State of Minnesota:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_soil_moisture_<date>
  ```

- **Download by County:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_soil_moisture_<date>_<countyname>
  ```
  *(Replace `<date>` with the desired year and month, and `<countyname>` with the desired county name (lower case, spaces replaced with '_'))*

  Available date range: **20237-20244 (July 2023 - April 2024)**

  For example:
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/get_soil_moisture_20237_hennepin
  ```
## Data Sources 
- **IEM**: Daily Min/Max temperature data.
- **NASA SMAP**: Soil Moisture.
- **TerraClimate**: Actual Evapotranspiration.
  
## Contributors 
- Tzu-Yu Ma  
- Samikshya Subedi
