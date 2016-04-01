##Comparing Backend Hosting

###Backend Hosting on CartoDB - Open Source
**Data ETL from Survos**  
After massaging and geocoding data, a python script can upload the shapefile to CartoDB PostGIS/PostgreSQL using a cartodb library or api (have to research).  

**Database:**  
PostGIS/PostgreSQL - Hosted on CartoDB's cloud. 

**Web Server:**  
AWS Apache / GeoServer - Hosted by CartoDB's Cloud.

  > **Pros:** Easy to use for testing  
**Cons:** Limited control; can't guaranteed security; cost $$ for private instance  

###Backend Hosting on NYU Stack - Open Source

**Data ETL from Survos**  
After massaging and geocoding data, a phython script can upload the shapefile to PostGIS/PostgreSQL using ogr2ogr or shploader commands.

**Database:**  
AWS PostGIS/PostgreSQL

**Web Server:**  
AWS Apache / GeoServer - Create WMS and WFS (web services) from data on PostGIS. Create SLDs for styling (quantile, point color, etc).

  > **Pros:** Free; Already have AWS; Can easily install LAPP; control of configuration, updates, and security  
**Cons:** Not as turn-key for dynamic analysis as ArcGIS Server; No user support help line  

###Backend Hosting on NYU Stack - ESRI  
**Data ETL from Survos**  
After massaging and geocoding data, a python script can upload the shapefile to SDE/PostgreSQL using arcpy library.

**Database:**  
AWS SDE/PostgreSQL  

**Web Server:**  
AWS Apache / ArcGIS Server - Create WMS and WFS (web services) from data on SDE. Create MXDs for styling (quantile, point color, etc) using ArcGIS interface.  

  > **Pros:**  Already have AWS; Can easily install LAPP; control of configuration, updates, and security, long experience with SDE/ArcGIS, lots of support, already built apis and ease of high-end analysis web services  
**Cons:** $$, Not open source, will require a separate build from a postgis/postgreql installation 

##Comparing Front-End Web Solutions

###Openlayers 3 - Open Source
With the upgrade to OpenLayers 3 in 2015, it has gotten a lot better. Can make multi-layer maps like in ESRI apis.  
Code: JavaScript, HTML, CSS, SQL PostgreSQL/PostGIS  
  * http://openlayers.org/
  * http://vasir.net/blog/openlayers/openlayers-tutorial-part-3-controls
  * Boundless has nice support docs: http://boundlessgeo.com/products/opengeo-suite/openlayers/
  
> **Pros:** great documentation and object library for creating a web interface similar to ESRI's. Boundless supports it. It's been around for a while (before Leaflet, MapBox, CartoDB). I built something with it 6 years ago - before version 3 was released.  
**Cons:** Not as hipster as CartoDB, Leaflet.  

###CartoDB - Open Source
Many people have used the CartoDB API's and libraries to create customized map apps.  Some people just use the backend for hosting because CartoDB implements a custom installation of PostGIS/PostgreSQL. See [this document](https://docs.google.com/document/d/1tutKhzrmon9YpGqIDH3vDPJnXDVPt5wG7SDSPXp9Ux4/edit#heading=h.48x7bb2w3y2o) for more on the inner workings of CartoDB's stack and pricing. 
Code: JavaScript, HTML, CSS, SQL PostgreSQL/PostGIS, CartoDB packages and libraries   
  * https://cartodb.com/gallery/
  * [Holly's NYU meeting with CartoDB - 2015](https://docs.google.com/document/d/1tutKhzrmon9YpGqIDH3vDPJnXDVPt5wG7SDSPXp9Ux4/edit#heading=h.48x7bb2w3y2o)

  > **Pros:**  Already have CartoDB account; easy to setup; great documentation; Holly has a personal relationship with the NYC office C-suite.  
**Cons:** $$; geocoding is not cheap (see Holly's meeting notes above); security could be a problem for IRB because using their backend; if CartoDB goes out of business - out of luck 

###Hybrid: CartoDB, Leaflet.js, MapBox.js - Open Source
This is a popular approach to creating customized map apps.  Once again, some people just use CartoDB as the backend.  
Code: JavaScript, jQuery, HTML, CSS, SQL PostgreSQL/PostGIS, CartoDB packages and libraries   
  * https://github.com/clhenrick/BushwickCommunityMap - can reverse engineer this as a guide.
  * https://www.mapbox.com/mapbox.js/example/v1.0.0/layers/

  > **Pros:**  Combines a lot of tools.  Good to have in-house knowledge of all these libraries, APIs.   
**Cons:** development time may be a bit longer than straight up CartoDB, but could be launched as a phase 3 development stage after proof of concept developed on CartoDB or OpenLayers.   

###ESRI JavaScript API - Proprietary
This is the same approach Andrew used with the Flex API (getting depracated) and the SilverLight API I developed in 5 years ago (also getting deprecated).     
  * https://developers.arcgis.com/javascript/

  > **Pros:**  Everything pretty much out of the box is sufficient to meet functional specs; Excellent phone support; ability to access high level analysis web services on backend data.  
**Cons:** $$; proprietary; most likely still requires using the ESRI stack (ArcGIS Server); ESRI (like all things) can be buggy/klunky. 

##Other Considerations

###Data Downloading / Cleaning  
Not sure if this falls under Survos. I've documented what knowledge I have gathered from documents Tom has provided and links Tac has provided. Need direction on how or if to proceed on the data cleaning strategy. 

Here is a link to the documentation I have started: 

###Geocoding  
This can be expensive. Here are some solutions:
  * With our Basic Plan, CartoDB charges 1K/mo included US$15/1k extra
  * ESRI - no longer included Geocoding with ArcGIS License. Have to use online Geocoding. I can check with my library friends to see how many service credits we have available at NYU. But from most of my discussions with other universities (Stanford, Columbia, Baruch, Pratt), the limit is hit pretty fast. ESRI's pricing/licensing is pretty confusing. See here: http://www.esri.com/software/arcgis/arcgisonline/credits  
  * Google Maps API geocoder - this used to be an open firehose, but Google put a stop to that a while back. Still can use it to geocode small batches through the API.
  * Lots of options for NYC area. I am documenting them here: [geocoding.md](/geocoding/geocoding.md)

###Responsive Design
I will have research this. I'm not sure how out of the box responsive design templates are with ESRI. I'd also have to research wrapping the mapping web-apps inside WordPress or Bootstrap responsive themes - and if they would play nicely. (http://getbootstrap.com/)  
