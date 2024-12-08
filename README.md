
# Houstin_Winter_Outages

**Title:** Analyzing the 2021 Texas Crisis with Night Lights and Socioeconomic Data.

**About:**
This project aims to analyze the impact of extreme winter storms on power outages in the Houston metropolitan area during February 2021. Using remotely-sensed night lights data and socioeconomic information, we will estimate the number of homes that lost power and investigate whether these impacts were disproportionately felt across different communities.

**Repository Structure:**

```
Houstin_Winter_Outage
│   README.md
│   Rmd/Proj files    
│
└───data
    │   gis_osm_buildings_a_free_1.gpkg
    │   gis_osm_roads_free_1.gpkg
    │
    └───ACS_2019_5YR_TRACT_48_TEXAS.gdb
    |   │   census tract gdb files
    |
    └───VNP46A1
    |   │   VIIRS data files
    |
    └───ejscreen
        |   EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb
```        

**Data:**
VIIRS data is distributed through NASA’s Level-1 and Atmospheric Archive & Distribution System Distributed Active Archive Center (LAADS DAAC). Many NASA Earth data products are distributed in 10x10 degree tiles in sinusoidal equal-area projection.

OpenStreetMap (OSM) is a collaborative project which creates publicly available geographic data of the world.We used Geofabrik’s download sites to retrieve a shapefile of all highways in Texas and prepared a Geopackage (.gpkg file) containing just the subset of roads that intersect the Houston metropolitan area. 

Obtained building data from OpenStreetMap. We again downloaded from Geofabrick and prepared a GeoPackage containing only houses in the Houston metropolitan area.

We obtained data from the U.S. Census Bureau’s American Community Survey for census tracts in 2019. The folder ACS_2019_5YR_TRACT_48.gdb is an ArcGIS “file geodatabase”, a multi-file proprietary format that’s roughly analogous to a GeoPackage file. When accessing data use st_layers() 
 
**References:**
U.S. Census Bureau ACS: United States Census Bureau. (2024). American Community Survey (ACS). Census.gov.Retrieved from https://www.census.gov/programs-surveys/acs

Geofabrik Data Downloads: Geofabrik GmbH. (2024). Geofabrik Download Server. Retrieved from https://download.geofabrik.de/

NASA MODAPS LAADS: NASA. (2024). LAADS DAAC: Level-1 and Atmosphere Archive & Distribution System. Retrieved from https://ladsweb.modaps.eosdis.nasa.gov/

United States Environmental Protection Agency. (2024). Purposes and Uses of EJSCREEN. EPA.gov.Retrieved from https://www.epa.gov/ejscreen/purposes-and-uses-ejscreen
