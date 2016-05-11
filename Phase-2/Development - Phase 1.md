
##Description  
**Hosted on AWS S3:** http://nyufda.com.s3-website-us-east-1.amazonaws.com/  
**Frontend:** Open source - CartoDB.js, Leaflet.js, MapBox.js, Google API, Bing Satellite Imagery  
**Backend:** CartoDB, local geojson   

####Time in Development
**Estimated Phase 1 development time:** 34 days  
**Actual development time:** 18 days  
[FDA Web App - GANTT Chart](https://docs.google.com/spreadsheets/d/1pGeYA_ZqB589tTHDEVeBk83pa6dXns9deqfT1emEtYU/edit#gid=0)   
<img src="/images/FDA_Gantt.png" width="500">

##Done:

**1. Violation Layers**  
- FDA Warning Letters - accessed from csv, geocoded, and infowindow with link to violation, only visible in zoom > 6
- FDA Civil Penalities - accessed from csv, geocoded, and infowindow with link to violation, only visible in zoom > 6
- FDA All violations - accessed from csv, geocoded, and created graduated circles, only visible in zoom <= 7

**2. Choropleth Layers**  
- FDA Contracts - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend
- State Synar Rates - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend
- Smokefree Laws - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend
- State Excise Tax - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend
- Youth Smoking Rates - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend
- Adult Smoking Rates - obatined new data, downloaded/cleaned, converted to spatial, created layer with popups and legend  

**3. Base Layers**
- Street Layer
- Satellite Layer

**4. Search by Address**

**5. Navigation Controls**

##In Progress:
- Refactoring Code: https://github.com/nyu-mhealth/FDA-WebApp-Code  

##To Do:  

####National Geocoding  
Here is the doc going in more detail: https://github.com/nyu-mhealth/GeoTools/blob/master/geocoding/geocoding.md  
- CartoDB
- QGIS
- ArcGIS (for NYC)
- Google API (Python with pause)

####Review Functionality  
- Separate selector for each violations layer?
- Select by and admin boundary? - this was in older app - but not sure purpose 
- other layers?


