##Comparing Backend Hosting

####Backend Hosting on NYU Stack
**Database:**  
AWS PostGIS/PostgreSQL - After massaging and geocoding data, a phython script can upload the shapefile to PostGIS/PostgreSQL using ogr2ogr or shploader commands.

**Web Server:**
AWS Apache / GeoServer - Create WMS and WFS (web services) from data on PostGIS. Create SLDs for styling (quantile, point color, etc).


