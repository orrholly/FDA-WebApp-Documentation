
###Fork Bushwick Community Mapper Github Repo

Fork https://github.com/clhenrick/BushwickCommunityMap to NYU mHealth org
Rename to 


###Setup SimpleHTTPServer on BushWick Directory

    cd
    cd Desktop/nyumhealth_git/FDA-WebApp-Code  
    python -m SimpleHTTPServer

Now just open a web browser and go to localhost:8000 To shut server down: got to terminal and hit cntrl + c


###Get Google Geocoding API Key (for address search)
https://developers.google.com/maps/documentation/geocoding/get-api-key#key

For IP Address: http://128.122.59.247:8000  
API Key: AIzaSyDj6Cz-The6dgtHU-4XSFxnEPe4VY-E9Ro  

**UPDATE** Do not need key anymore for geocoding with Google - although there is a 2500 free limit a day https://developers.google.com/maps/documentation/geocoding/usage-limits  

Instead use this snippet:  

          <script src="http://maps.google.com/maps/api/js?v=3&sensor=false"></script> 

###Code Research

**CartoDB.js**
http://academy.cartodb.com/courses/cartodbjs-ground-up/createvis-vs-createlayer/

###Fron Chris code - the important bits:  
####main.js  
css switching  

    var changeCartoCSS = function(layer, css) {
        layer.setCartoCSS(css);
      };
  
sql switching 

    // change SQL query of a layer
    var changeSQL = function(layer, sql) {
      layer.setSQL(sql);
    }
  
This is where it all starts : 
    
      // get it all going!
      var init = function() {
        initMap();
        initButtons();
        initCheckboxes();
        searchAddress();
        initZoomButtons();
        app.intro.init();  
        
This is where I setup queireis:

        //HOLLY - comment out
          // queries for warning types
          // sent to cartodb when layer buttons clicked
          el.sql = {
            all : "SELECT * FROM allwarnings_dc1",
            warningLetters : "SELECT * FROM allwarnings_dc1 WHERE decisiontype = 'Warning Letter'",
            civilPenalty : "SELECT * FROM bushwick_pluto14v1 WHERE decisiontype = 'Civil Money Penalty'",
          };
  
  ####mapstyles.js  
  This is where all the css is for each layer
  
  ####change buttons in all these locations

        /Users/hollyorr/Desktop/nyumhealth_git/FDA-WebApp-Code/js/main_orig.js:
          280: availfar : function() {
        
        /Users/hollyorr/Desktop/nyumhealth_git/FDA-WebApp-Code/index_orig.html:
          40: <a href="#availfar" id="availfar" class="button">
        
        /Users/hollyorr/Desktop/nyumhealth_git/FDA-WebApp-Code/js/main.js:
          280: availfar : function() {
        
        /Users/hollyorr/Desktop/nyumhealth_git/FDA-WebApp-Code/index.html:
          40: <a href="#availfar" id="availfar" class="button">
        
        /Users/hollyorr/Desktop/nyumhealth_git/FDA-WebApp-Code/js/intro.js:
          96: el.taxLotActions['availfar']();
          
    Replaced all taxLots variables with warningpts
    
### Use Mapbox basemap  

Account is saved in CGPH LastPass  
public access token: pk.eyJ1Ijoibnl1bWhlYWx0aCIsImEiOiJjaW5xMXU5d2IxMDlldWdseW9zbXl3dG94In0.pC5lMAc_tKvgtUcHquXuwg  

### Create separate layers for violations points (viz vs createlayer)  
http://bl.ocks.org/clhenrick/5928c5328b416dcb4c88  
http://bl.ocks.org/xavijam/7283a403afb6a54eda9a  
http://academy.cartodb.com/courses/cartodbjs-ground-up/createvis-vs-createlayer/  
http://gis.stackexchange.com/questions/83092/how-do-you-create-a-cartodb-viz-with-a-dynamic-sql-statement  
http://gis.stackexchange.com/questions/108656/how-to-add-multiple-cartodb-layers-in-viz-json-to-a-leaflet-layer-control  
http://byndhack.herokuapp.com/  
http://docs.cartodb.com/tutorials/custom_interactivity/  


