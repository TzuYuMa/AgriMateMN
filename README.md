![logo](https://github.com/TzuYuMa/AgriMateMN/blob/main/logo/logo.png)

# AgriMateMN APP
![GitHub last commit](https://img.shields.io/github/last-commit/TzuYuMa/AgriMateMN?style=for-the-badge)

## Overview  
AgriMateMN provides AGDD (Accumulated Growing Degree Days) data for the Last Minnesota Growing Season (May-Sep 2023), Soil Moisture data from July 2023 to April 2024, and ET (Actual Evapotranspiration) data from May 2023 to September 2023. Selecting the desire area to download data with CSV or PDF file, or you can find the [Data URLs for GeoJson](#data-urls-for-geojson) utilizing GeoJSON format from APIs. This supports agricultural decision-making in Minnesota by facilitating the comparison of various models for accurate analysis.

## Data URLs for GeoJson
### AGDD Data
- **Download for Entire State of Minnesota:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/agdd/minnesota
  ```

- **Download by County:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/agdd/<county>
  ```
  *(Replace `<county>` with the desired county name (lower case, spaces replaced with '_'))*

  For example:
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/agdd/st_louis
  ```

  *Data Coverage: Previous growing season, spanning from April 2023 to September 2023. Utilizes Inverse Distance Weighted (IDW) interpolation based on 153 observation sites across Minnesota.*

### ET Data
- **Download for Entire State of Minnesota:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/et/<date>
  ```

- **Download by County:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/et/<date>/<countyname>
  ```
  *(Replace `<date>` with the desired year and month, and `<countyname>` with the desired county name (lower case, spaces replaced with '_'))*

  Available date range: **20235-20239 (May 2023 - September 2023)**

  For example:
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/et/20237/st_louis
  ```

### Soil Moisture Data
- **Download for Entire State of Minnesota:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/soil_moisture/<date>
  ```

- **Download by County:**
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/soil_moisture/<date>/<countyname>
  ```
  *(Replace `<date>` with the desired year and month, and `<countyname>` with the desired county name (lower case, spaces replaced with '_'))*

  Available date range: **20237-20244 (July 2023 - April 2024)**

  For example:
  ```plaintext
  https://googlecloudrun-nvrttyom5q-uc.a.run.app/soil_moisture/20237/st_louis
## Minnesota Counties

|        |        |        |        |        |
|--------|--------|--------|--------|--------|
| Aitkin | Anoka  | Becker | Beltrami | Benton |
| Big Stone | Blue Earth | Brown | Carlton | Carver |
| Cass | Chippewa | Chisago | Clay | Clearwater |
| Cook | Cottonwood | Crow Wing | Dakota | Dodge |
| Douglas | Faribault | Fillmore | Freeborn | Goodhue |
| Grant | Hennepin | Houston | Hubbard | Isanti |
| Itasca | Jackson | Kanabec | Kandiyohi | Kittson |
| Koochiching | Lac qui Parle | Lake | Lake of the Woods | Le Sueur |
| Lincoln | Lyon | McLeod | Mahnomen | Marshall |
| Martin | Meeker | Mille Lacs | Morrison | Mower |
| Murray | Nicollet | Nobles | Norman | Olmsted |
| Otter Tail | Pennington | Pine | Pipestone | Polk |
| Pope | Ramsey | Red Lake | Redwood | Renville |
| Rice | Rock | Roseau | St. Louis | Scott |
| Sherburne | Sibley | Stearns | Steele | Stevens |
| Swift | Todd | Traverse | Wabasha | Wadena |
| Waseca | Washington | Watonwan | Wilkin | Winona |
| Wright | Yellow Medicine |        |        |        |

## Data Sources 
- [**Iowa Environmental Mesonet (IEM)**](https://mesonet.agron.iastate.edu/): Daily Min/Max temperature data.
- [**NASA SMAP**](https://nsidc.org/data/spl3smp_e/versions/3): Soil Moisture.
- [**TerraClimate**](https://developers.google.com/earth-engine/datasets/catalog/IDAHO_EPSCOR_TERRACLIMATE): Actual Evapotranspiration.
  
## Contributors 
- Tzu-Yu Ma  
- Samikshya Subedi
