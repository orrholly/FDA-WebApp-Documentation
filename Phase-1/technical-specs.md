##Comparing Backend Hosting

###Backend Hosting on CartoDB - Open Source

**Database:**  
PostGIS/PostgreSQL - Hosted on CartoDB's cloud. 

**Web Server:**  
AWS Apache / GeoServer - Hosted by CartoDB's Cloud.

  > Pros: Easy to use for testing  
Cons: Limited control; can't guaranteed security; cost $$ for private instance  

###Backend Hosting on NYU Stack - ESRI  
**Data ETL from Survos**  
After massaging and geocoding data, a python script can upload the shapefile to SDE/PostgreSQL using arcpy library.

**Database:**  
AWS SDE/PostgreSQL  

**Web Server:**  
AWS Apache / ArcGIS Server - Create WMS and WFS (web services) from data on SDE. Create MXDs for styling (quantile, point color, etc) using ArcGIS interface.  

  > Pros: Free; Already have AWS; Can easily install LAPP; control of configuration, updates, and security  
Cons: Not as turn-key for dynamic analysis as ArcGIS Server; No user support help line  

###Backend Hosting on NYU Stack - Open Source

**Database:**  
AWS PostGIS/PostgreSQL - After massaging and geocoding data, a phython script can upload the shapefile to PostGIS/PostgreSQL using ogr2ogr or shploader commands.

**Web Server:**  
AWS Apache / GeoServer - Create WMS and WFS (web services) from data on PostGIS. Create SLDs for styling (quantile, point color, etc).

  > Pros: Free; Already have AWS; Can easily install LAPP; control of configuration, updates, and security  
Cons: Not as turn-key for dynamic analysis as ArcGIS Server; No user support help line  
